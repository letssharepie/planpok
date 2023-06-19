<template>
  <div class="card-container">
    <Card :fibonacciNumber="number" v-for="number in fibonacci" :key="number" />
  </div>
</template>

<script>
import Card from "~/components/Card.vue";
import fibonacci from "../static/fibonacci.json";

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
  grid-gap: 10px;
}
</style>
