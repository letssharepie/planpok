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
  grid-template-columns: repeat(5, minmax(200px, 1fr));
  grid-gap: 20px;
  justify-content: center;
  align-items: center;
  padding-top: 20px;
}

.card-container:last-child {
  justify-content: flex-start;
}

@media (max-width: 768px) {
  .card-container {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (max-width: 480px) {
  .card-container {
    grid-template-columns: repeat(2, 1fr);
  }
}
</style>
