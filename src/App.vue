<template>
  <div class="container-fluid p-0 m-0">
    <navbar></navbar>
    <main>
      <!-- carousel -->
      <home-carousel></home-carousel>
    </main>
  </div>
</template>

<script>
import navbar from "./components/Navbar.vue";
import HomeCarousel from "./components/HomeCarousel.vue";

export default {
  components: {
    navbar,
    "home-carousel": HomeCarousel,
  },
};
</script>

<style></style>
