<template>
  <div class="container-fluid p-0 m-0">
    <navbar></navbar>
    <main>
      <!-- carousel -->
      <div class="container-fluid px-0 py-8 py-md-5" id="carousel-container">
        <home-carousel></home-carousel>
      </div>
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

<style>
#carousel-container {
  background-image: url("./assets/main-carousel-bg.jpg");
  background-repeat: repeat;
}
</style>
