<template>
  <div>
    <b-card class="card-main">
      <b-card-title class="card-title">
        {{ fibonacciNumber }}
      </b-card-title>
      <b-card-footer>
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
.card-main {
  width: 200px;
  height: 300px;
}

.card-title {
  text-align: center;
}
</style>
