<template>
  <div class="card-container">
    <Card v-for="number in fibonacci" :fibonacciNumber="number" :key="number" />
  </div>
</template>

<script>
import fibonacci from "../static/fibonacci.json";
import Card from "./Card.vue";

export default {
  components: {
    Card,
  },
  data() {
    return {
      fibonacci: fibonacci,
    };
  },
};
</script>

<style>
.card-container {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
}
</style>
