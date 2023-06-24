<template>
  <b-modal
    v-model="modalValue"
    @ok="submitNickname"
    title="Enter Your Nickname"
  >
    <form @submit="submitNickname">
      <b-form-group label="Nickname">
        <b-form-input v-model="nickname" required></b-form-input>
      </b-form-group>
    </form>
  </b-modal>
</template>

<script>
export default {
  data() {
    return {
      nickname: "",
    };
  },
  props: {
    value: {
      type: Boolean,
      required: true,
    },
  },
  computed: {
    modalValue: {
      get() {
        return this.value;
      },
      set(newValue) {
        this.$emit("input", newValue);
      },
    },
  },
  methods: {
    submitNickname(event) {
      event.preventDefault();
      this.$emit("nickname-submitted", this.nickname);
      this.nickname = "";
    },
  },
};
</script>

<style scoped>
.modal-footer {
  display: flex;
  justify-content: flex-end;
  margin-top: 20px;
}
</style>
