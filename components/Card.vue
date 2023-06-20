<template>
  <div>
    <b-card class="card-main">
      <b-card-title class="card-title">
        {{ fibonacciNumber }}
      </b-card-title>
      <b-card-footer class="card-footer" bottom>
        <b-button variant="primary">Select</b-button>
      </b-card-footer>
    </b-card>
  </div>
</template>

<script>
export default {
  props: {
    fibonacciNumber: {
      type: Number,
      required: true,
    },
  },
};
</script>

<style>
div {
  padding: 20px;
}

.card-main {
  width: 200px;
  height: 300px;
  padding: 20px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.card-title {
  text-align: center;
}
</style>
