<template>
  <div>
    <b-card @click="openModal" class="card-main" tag="button">
      <b-card-title class="card-title">
        {{ fibonacciNumber }}
      </b-card-title>
    </b-card>

    <b-modal v-model="showModal" title="Selected Number">
      <p>You picked number {{ fibonacciNumber }}</p>
      <template #modal-footer>
        <b-button variant="primary" @click="closeModal">OK</b-button>
      </template>
    </b-modal>
  </div>
</template>

<script>
export default {
  props: {
    fibonacciNumber: {
      type: [Number, String],
      required: true,
    },
  },
  data() {
    return {
      showModal: false,
    };
  },
  methods: {
    openModal() {
      this.showModal = true;
    },
    closeModal() {
      this.showModal = false;
    },
  },
};
</script>

<style>
.card-main {
  width: 200px;
  height: 300px;
  margin: auto;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background-color: #f0f0f0;
  border-radius: 8px;
  cursor: pointer;
  transition: background-color 0.2s ease;
}

.card-main:hover {
  background-color: #707070;
}

.card-title {
  text-align: center;
  font-size: 24px;
  font-weight: bold;
  color: #333333;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

.b-modal {
  text-align: center;
}

.b-modal-header {
  background-color: #f0f0f0;
  border-bottom: none;
}

.b-modal-body {
  padding: 20px;
}

.b-modal-footer {
  background-color: #f0f0f0;
  border-top: none;
  display: flex;
  justify-content: center;
}
</style>
