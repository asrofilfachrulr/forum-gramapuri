<template>
  <div class="container-fluid p-0 m-0">
    <basic-info-modal :typeInfo="modalInfoType"></basic-info-modal>
    <navbar @modal-type-info="setModalInfo"></navbar>
    <main>
      <!-- carousel -->
      <home-carousel></home-carousel>
      <!-- sections -->
      <home-section
        :innerComponent="newsSection"
        @modal-type-info="setModalInfo"
      ></home-section>
    </main>
  </div>
</template>

<script>
import navbar from "./components/Navbar.vue";
import HomeCarousel from "./components/HomeCarousel.vue";
import HomeSection from "./components/HomeSection.vue";
import NewsHomeSection from "./components/NewsHomeSection.vue";
import BasicInfoModal from "./components/BasicInfoModal.vue";

export default {
  components: {
    navbar,
    "home-carousel": HomeCarousel,
    "home-section": HomeSection,
    "basic-info-modal": BasicInfoModal,
  },
  data() {
    return {
      newsSection: NewsHomeSection,
      modalInfoType: "",
    };
  },
  methods: {
    setModalInfo(value) {
      console.log("received modal-type-info event on App with value", value);
      this.modalInfoType = value;
    },
  },
};
</script>

<style></style>
