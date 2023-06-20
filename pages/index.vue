<template>
  <div class="container">
    <b-row>
      <Navbar class="navbar" />
    </b-row>
    <b-row>
      <b-col cols="10">
        <Deck />
      </b-col>

      <b-col cols="2">
        <Sidebar />
      </b-col>
    </b-row>
    <b-row>
      <b-col>
        <Footer />
      </b-col>
    </b-row>
  </div>
</template>

<script>
import Deck from "~/components/Deck.vue";
import Navbar from "~/components/Navbar.vue";
import Sidebar from "~/components/Sidebar.vue";
import Footer from "~/components/Footer.vue";

export default {
  components: {
    Deck,
    Navbar,
    Sidebar,
    Footer,
  },
};
</script>

<style>
.container {
  display: flex;
  flex-direction: column;
  width: 100%;
  max-width: 100%;
}

.content {
  display: flex;
}

.navbar {
  width: 100%;
}
</style>
