<template>
  <div class="container-fluid p-0 m-0">
    <basic-info-modal :typeInfo="modalInfoType"></basic-info-modal>
    <navbar @modal-type-info="setModalInfo"></navbar>
    <main>
      <!-- carousel -->
      <home-carousel></home-carousel>
      <!-- sections -->

      <!-- about -->
      <home-section :innerComponent="aboutSection"></home-section>

      <!-- news -->
      <!-- <home-section
        :innerComponent="newsSection"
        @modal-type-info="setModalInfo"
      >
      </home-section> -->
    </main>
  </div>
</template>

<script>
import navbar from "./components/Navbar.vue";
import HomeCarousel from "./components/HomeCarousel.vue";
import HomeSection from "./components/HomeSection.vue";
// import NewsHomeSection from "./components/NewsHomeSection.vue";
import BasicInfoModal from "./components/BasicInfoModal.vue";
import AboutSection from "./components/AboutSection.vue";
import { shallowRef } from "vue";

export default {
  components: {
    navbar,
    "home-carousel": HomeCarousel,
    "home-section": HomeSection,
    "basic-info-modal": BasicInfoModal,
  },
  data() {
    return {
      // newsSection: shallowRef(NewsHomeSection),
      aboutSection: shallowRef(AboutSection),
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

<style>
:root {
  --clr-accent: #0a4d1f;
  --clr-accent-light: #60af79;
}

.underline-accent {
  position: relative;
}

.underline-accent::after {
  content: "";
  border: 2px solid var(--clr-accent);
  border-radius: 10px;
  height: 0px;
  width: 75%;
  left: 0;
  right: 0;
  margin: auto;
  bottom: 0;
  position: absolute;
}

.text-accent {
  color: var(--clr-accent);
}

.text-accent-light {
  color: var(--clr-accent-light);
}

.cover-dim {
  position: relative;
}

.cover-dim::before {
  display: block;
  position: absolute;
  content: "";
  z-index: 2;
  background-color: rgba(0, 0, 0, 0.35);
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.cover-accent-on-hover {
  transition: all 200ms ease-in-out;
}

.cover-accent-on-hover:hover {
  background-color: rgba(96, 175, 121, 0.15);
  border-color: transparent;
}
</style>
