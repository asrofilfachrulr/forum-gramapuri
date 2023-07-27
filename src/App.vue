<template>
  <div class="container-fluid p-0 m-0">
    <navbar></navbar>
    <main>
      <!-- carousel -->
      <home-carousel></home-carousel>
      <!-- sections -->
      <home-section :innerComponent="newsSection"></home-section>
    </main>
  </div>
</template>

<script>
import navbar from "./components/Navbar.vue";
import HomeCarousel from "./components/HomeCarousel.vue";
import HomeSection from "./components/HomeSection.vue";
import NewsHomeSection from "./components/NewsHomeSection.vue";

export default {
  components: {
    navbar,
    "home-carousel": HomeCarousel,
    "home-section": HomeSection,
  },
  data() {
    return {
      newsSection: NewsHomeSection,
    };
  },
};
</script>

<style></style>
