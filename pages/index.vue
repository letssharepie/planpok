<template>
  <div class="container">
    <h1>Welcome to Planning Poker!</h1>
    <b-button variant="primary" @click="createRoom">Create a room</b-button>

    <NicknameModal
      :value="showModal"
      @input="showModal = $event"
      @nickname-submitted="handleNicknameSubmit"
    />
  </div>
</template>

<script>
import NicknameModal from "~/components/NicknameModal.vue";

export default {
  data() {
    return {
      showModal: false,
      roomId: "",
      nickname: "",
    };
  },
  methods: {
    createRoom() {
      this.roomId = Date.now().toString();

      // Show the nickname modal
      this.showModal = true;
    },
    handleNicknameSubmit(nickname) {
      if (nickname.trim() !== "") {
        this.roomId = Date.now().toString();

        this.nickname = nickname;

        this.$router.push(`/${this.roomId}`);
      }
    },
  },
  components: {
    NicknameModal,
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
}

h1 {
  margin-bottom: 20px;
}
</style>
