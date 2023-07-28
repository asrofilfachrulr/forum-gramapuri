<template>
  <div class="container my-5">
    <div class="row mb-5">
      <div class="col-12 d-flex justify-content-center">
        <h1 class="ff-condensed py-3 underline-accent d-inline" id="about">
          Tentang Kami
        </h1>
      </div>
    </div>
    <div class="row row-gap-4 px-4">
      <div
        class="row row-gap-4 column-gap-4 p-0 m-0 justify-content-center align-items-center"
        style="height: max-content"
      >
        <div class="col-12 p-0 col-md-4 col-lg-4 h-100">
          <card-basic
            :class="'cover-accent-on-hover'"
            :heightSize="'400px'"
            :innerHtml="cardContentsToHtml(cardContents[0])"
          ></card-basic>
        </div>
        <div class="col-12 p-0 col-md-4 col-lg-4 h-100">
          <card-basic
            :class="'cover-accent-on-hover'"
            :heightSize="'400px'"
            :innerHtml="cardContentsToHtml(cardContents[1])"
          ></card-basic>
        </div>
      </div>
      <div
        class="row row-gap-4 column-gap-4 p-0 m-0 justify-content-center align-items-center"
        style="height: max-content"
      >
        <div class="col-12 p-0 col-md-4 col-lg-4 h-100">
          <card-basic
            :class="'cover-accent-on-hover'"
            :heightSize="'400px'"
            :innerHtml="cardContentsToHtml(cardContents[2])"
          ></card-basic>
        </div>
        <div class="col-12 p-0 col-md-4 col-lg-4 h-100">
          <card-basic
            :class="'cover-accent-on-hover'"
            :heightSize="'400px'"
            :innerHtml="cardContentsToHtml(cardContents[3])"
          ></card-basic>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import CardBasic from "./CardBasic.vue";
export default {
  components: {
    "card-basic": CardBasic,
  },
  data() {
    return {
      cardContents: [
        {
          img: "https://img.icons8.com/pulsar-color/48/google-maps.png",
          content:
            "Kami organisasi lokal bertempat di <span class='text-accent fw-bold'>Perum. Gramapuri Persada Blok E</span>, Desa Sukajaya, Cibitung, Kabupaten Bekasi",
        },
        {
          img: "https://img.icons8.com/pulsar-color/48/trust.png",
          content:
            "Kami percaya bahwa setiap perbuatan baik, <span class='text-accent fw-bold'>sekecil apapun</span>, memberikan dampak positif yang besar bagi sesama",
        },
        {
          img: "https://img.icons8.com/pulsar-color/48/parallel-tasks.png",
          content:
            "Kami adalah bagian dari <span class='text-accent fw-bold'>kepengurusan RT</span> yang bertanggung jawab untuk mengelola dan mengurusi kegiatan sedekah Jumat dan sedekah lainnya dalam lingkungan kami",
        },
        {
          img: "https://img.icons8.com/pulsar-color/48/fire-element.png",
          content:
            "Motivasi kami adalah mewujudkan semangat gotong royong. Kami <span class='text-accent fw-bold'>berkomitmen untuk selalu berkontribusi</span> dalam solidaritas sosial untuk kehidupan yang lebih baik",
        },
      ],
    };
  },
  methods: {
    cardContentsToHtml(card) {
      return `<div class="d-flex justify-content-center"><img class='mb-3' src='${card.img}'/></div><p>${card.content}</p>`;
    },
  },
};
</script>

<style></style>
