<template>
  <div class="container p-0">
    <div class="row row-gap-3 p-4 p-md-0 d-flex justify-content-center">
      <div class="col-12 col-md-8 col-lg-6">
        <div
          id="carouselExampleAutoplaying"
          class="carousel slide rounded-md-custom"
          style="overflow: hidden"
          data-bs-ride="carousel"
          data-bs-interval="4000"
        >
          <div class="carousel-inner cover-dim" id="carousel-inner-home">
            <div class="carousel-item active">
              <img
                src="https://unsplash.com/photos/kZ1zThg6G40/download?ixid=M3wxMjA3fDB8MXxhbGx8fHx8fHx8fHwxNjkwNDE0NTA4fA&force=true&w=1920"
                class="d-block w-100 position-relative"
                alt="..."
              />
            </div>
            <div class="carousel-item">
              <img
                src="https://unsplash.com/photos/mWxKMCLtnyw/download?ixid=M3wxMjA3fDB8MXxhbGx8fHx8fHx8fHwxNjkwNDE0NTQ3fA&force=true&w=1920"
                class="d-block w-100 position-relative"
                alt="..."
              />
            </div>
            <div class="carousel-item">
              <img
                src="https://unsplash.com/photos/lZOGde6okcA/download?ixid=M3wxMjA3fDB8MXxzZWFyY2h8NDR8fG1vc3F1ZXxlbnwwfHx8fDE2OTAzNTQ3ODB8MA&force=true&w=1920"
                class="d-block w-100 position-relative"
                alt="..."
              />
            </div>
          </div>
          <button
            class="carousel-control-prev"
            type="button"
            data-bs-target="#carouselExampleAutoplaying"
            data-bs-slide="prev"
          >
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
          </button>
          <button
            class="carousel-control-next"
            type="button"
            data-bs-target="#carouselExampleAutoplaying"
            data-bs-slide="next"
          >
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
          </button>
        </div>
      </div>
      <div class="col-12 col-md-4 col-lg-3">
        <div class="row row-gap-2" id="row-parallel-with-home-carousel">
          <div class="col-6 col-md-12">
            <img
              src="https://www.gramapuripersada.com/wp-content/uploads/2020/06/LOGO-GRAMAPURI-SOSMED-1024x1024.jpg"
              alt=""
              class="d-block rounded-md-custom w-100"
              style="object-fit: cover"
            />
          </div>
          <div class="col-6 col-md-12">
            <img
              src="../assets/gerbang-gramapuri-1024x768.jpg"
              alt=""
              class="d-block rounded-md-custom w-100"
              style="object-fit: cover"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {},
};
</script>

<style>
/* Custom CSS */
.rounded-md-custom {
  border-radius: 0.5rem; /* Set the desired border radius for "md" and above */
}

@media (max-width: 768px) {
  #row-parallel-with-home-carousel img {
    max-height: 160px;
  }
}

@media (min-width: 768px) {
  #row-parallel-with-home-carousel img {
    height: 152px;
  }
}
@media (min-width: 992px) {
  #row-parallel-with-home-carousel img {
    height: 152px;
  }
}
@media (min-width: 1200px) {
  #row-parallel-with-home-carousel img {
    height: 185px;
  }
}
@media (min-width: 1400px) {
  #row-parallel-with-home-carousel img {
    height: 215px;
  }
}

#carouselExampleAutoplaying .carousel-inner {
  overflow: hidden;
}

#carouselExampleAutoplaying img {
  object-fit: cover;
}

.cover-dim {
  position: relative;
}

.cover-dim::before {
  display: block;
  position: absolute;
  content: "";
  z-index: 99;
  background-color: rgba(0, 0, 0, 0.35);
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

#carouselExampleAutoplaying button {
  z-index: 9;
}
</style>
