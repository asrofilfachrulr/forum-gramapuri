<template>
  <div class="container pt-3 pb-5" id="visi-misi">
    <div class="row pb-5">
      <div class="col-12 d-flex justify-content-center py-4">
        <h1 class="ff-condensed underline-accent py-3">Visi & Misi</h1>
      </div>
      <div class="col-12">
        <div class="row row-gap-4">
          <div
            class="col-12 col-md-6 col-lg-3"
            v-for="(card, index) in cardContents"
            :key="index"
          >
            <component
              :is="cardBasic"
              :innerHtml="cardContentsToHtml(card)"
              :class="'card-floated-on-hover'"
            ></component>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { shallowRef } from "vue";
import CardBasic from "./CardBasic.vue";
export default {
  data() {
    return {
      cardBasic: shallowRef(CardBasic),
      cardContents: [
        {
          title: "Kesejahteraan",
          subtitle:
            '<span class="text-accent fw-bold">Mengurangi kesulitan dan penderitaan</span> yang dialami oleh mereka yang kurang beruntung',
        },
        {
          title: "Kemandirian",
          subtitle: `<span class="text-accent fw-bold">Pemberdayaan dalam pengembangan potensi</span> dan perubahan hidup secara berkelanjutan`,
        },
        {
          title: "Solidaritas",
          subtitle: `<span class="text-accent fw-bold">Membangun ikatan sosial</span> yang kuat dan menciptakan kesadaran akan tanggung jawab`,
        },
        {
          title: "Keimanan",
          subtitle: `<span class="text-accent fw-bold">Pengajaran diri</span> untuk perendahan hati, empati sosial, dan rasa syukur terhadap karunia yang telah terima`,
        },
      ],
    };
  },
  methods: {
    cardContentsToHtml(card) {
      return `<div class="d-flex justify-content-center"><p class='mb-3 fs-4 fw-bold'>${card.title}</p></div><p style="color: var(--bs-card-color)">${card.subtitle}</p>`;
    },
  },
};
</script>

<style>
.card-floated-on-hover {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: all 0.2s ease;
  border-color: transparent;
  position: relative;
}

.card-floated-on-hover:hover {
  cursor: pointer;
  transform: translateY(-5px);
}

.card-floated-on-hover::after {
  display: block;
  content: "";
  width: 100%;
  height: 100%;
  background-color: transparent;
  position: absolute;
  top: 0;
  left: 0;
  transition: all 0.2s ease-out;
}

.card-floated-on-hover:hover::after {
  border-radius: 7px;
  border: 3px solid var(--clr-accent);
}
</style>
