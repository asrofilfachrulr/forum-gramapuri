<template>
  <div class="container">
    <div class="row">
      <div class="col-12 d-flex justify-content-between align-items-end">
        <h1 class="m-0">Berita</h1>
        <a
          class="link-dark link-offset-2 link-underline-opacity-25 link-underline-opacity-100-hover"
          href="#"
          data-bs-toggle="modal"
          data-bs-target="#basic-info-modal"
          @click="emitMaintenanceModal"
          >Lihat Semua →</a
        >
      </div>
    </div>

    <div class="row position-relative">
      <div
        class="row flex-nowrap py-4 scroll-container"
        style="overflow: auto hidden"
        id="news-card-horizontal-list"
      >
        <component
          :is="cardNews"
          v-for="index in 10"
          :key="index"
          data-bs-toggle="modal"
          data-bs-target="#basic-info-modal"
          @click="emitMaintenanceModal"
        >
        </component>
      </div>
    </div>
  </div>
</template>

<script>
import CardNews from "./ExampleCardNews.vue";
import { shallowRef } from "vue";

export default {
  data() {
    return {
      cardNews: shallowRef(CardNews),
    };
  },
  methods: {
    emitMaintenanceModal() {
      console.log(
        "emitted modal-type-info from navbar with value 'maintenance'"
      );
      this.$emit("modal-type-info", "maintenance");
    },
  },
};
</script>

<style>
.scroll-container {
  overflow-x: auto; /* Enable horizontal scrolling */
  scrollbar-width: thin; /* Set the width of the scrollbar */
  scrollbar-color: #888888 #f0f0f0; /* Set the color of the scrollbar */
}

/* Style the scrollbar track */
.scroll-container::-webkit-scrollbar {
  width: 10px; /* Set the width of the scrollbar */
  height: 10px;
}

/* Style the scrollbar thumb */
.scroll-container::-webkit-scrollbar-thumb {
  background-color: #888888; /* Set the color of the scrollbar thumb */
  border-radius: 3px; /* Rounded corners for the scrollbar thumb */
}

.scroll-container::-moz-scrollbar {
  width: 10px;
  height: 10px;
}

.scroll-container::-moz-scrollbar-thumb {
  background-color: #888888;
  border-radius: 3px;
}

.btn-custom-icon-rounded {
  height: min-content;
  width: min-content;
  padding: 0;
  margin: 0;
  border: none;
  border-radius: 100%;
  background-color: white;
}

#news-card-horizontal-list::-webkit-scrollbar {
  display: none;
  width: 0 !important;
}

#news-card-horizontal-list {
  -ms-overflow-style: none;
  scrollbar-width: none;
}
</style>
