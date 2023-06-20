<template>
  <div>
    <Deck />
  </div>
</template>

<script>
import Deck from "~/components/Deck.vue";

export default {
  components: {
    Deck,
  },
};
</script>

<style>
.card-container {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
}
</style>
