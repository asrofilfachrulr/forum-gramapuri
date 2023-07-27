<template>
  <div class="container-fluid px-0 py-0 py-md-5" id="carousel-container">
    <div class="container p-0">
      <div class="row row-gap-3 p-4 p-md-0 d-flex justify-content-center">
        <div class="col-12 col-md-8 col-lg-8">
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
                  src="https://unsplash.com/photos/kjvVr6IQAxQ/download?ixid=M3wxMjA3fDB8MXxzZWFyY2h8NjV8fG1hc2ppZHxlbnwwfDB8fHwxNjkwNDQ5NDQwfDI&force=true&w=1920"
                  class="d-block w-100 position-relative"
                  alt="..."
                />
                <div class="carousel-caption d-block">
                  <p>
                    “Sesungguhnya sedekah itu memadamkan murka Allah dan menolak
                    mati jelek (su’ul khotimah).” (HR Thabrani)
                  </p>
                </div>
              </div>
              <div class="carousel-item">
                <img
                  src="https://unsplash.com/photos/mWxKMCLtnyw/download?ixid=M3wxMjA3fDB8MXxhbGx8fHx8fHx8fHwxNjkwNDE0NTQ3fA&force=true&w=1920"
                  class="d-block w-100 position-relative"
                  alt="..."
                />
                <div class="carousel-caption d-block">
                  <p>
                    “Wahai Aisyah, halangilah dirimu dari neraka meskipun dengan
                    sebiji kurma, karena hal itu bisa menutupi orang lapar dari
                    kelaparan.” (HR Thabrani)
                  </p>
                </div>
              </div>
              <div class="carousel-item">
                <img
                  src="https://unsplash.com/photos/VbU9cVZ5Dh4/download?ixid=M3wxMjA3fDB8MXxzZWFyY2h8N3x8YmFuZHVuZ3xlbnwwfHx8fDE2OTA0NDYxOTd8MA&force=true&w=1920"
                  class="d-block w-100 position-relative"
                  alt="..."
                />
                <div class="carousel-caption d-block">
                  <p>
                    "Allah memusnahkan riba dan menyuburkan sedekah. Allah tidak
                    menyukai setiap orang yang tetap dalam kekafiran dan
                    bergelimang dosa.” (QS. Al-Baqarah: 276).
                  </p>
                </div>
              </div>
            </div>
            <button
              class="carousel-control-prev"
              type="button"
              data-bs-target="#carouselExampleAutoplaying"
              data-bs-slide="prev"
            >
              <span
                class="carousel-control-prev-icon"
                aria-hidden="true"
              ></span>
              <span class="visually-hidden">Previous</span>
            </button>
            <button
              class="carousel-control-next"
              type="button"
              data-bs-target="#carouselExampleAutoplaying"
              data-bs-slide="next"
            >
              <span
                class="carousel-control-next-icon"
                aria-hidden="true"
              ></span>
              <span class="visually-hidden">Next</span>
            </button>
          </div>
        </div>
        <div class="col-12 col-md-4 col-lg-4">
          <div class="row row-gap-2" id="row-parallel-with-home-carousel">
            <div class="col-6 col-md-12" style="overflow: hidden">
              <div class="cover-dim rounded-md-custom" style="overflow: hidden">
                <img
                  src="https://www.gramapuripersada.com/wp-content/uploads/2020/06/LOGO-GRAMAPURI-SOSMED-1024x1024.jpg"
                  alt=""
                  class="d-block w-100"
                  style="object-fit: cover"
                />
                <div
                  class="position-absolute top-0 w-100 h-100 d-flex justify-content-center align-items-center"
                  style="z-index: 4"
                >
                  <a href="https://www.gramapuripersada.com/" target="_blank">
                    <button type="button" class="btn btn-outline-light">
                      Homepage
                    </button>
                  </a>
                </div>
              </div>
            </div>
            <div class="col-6 col-md-12" style="overflow: hidden">
              <div class="cover-dim rounded-md-custom" style="overflow: hidden">
                <img
                  src="../assets/gerbang-gramapuri-1024x768.jpg"
                  alt=""
                  class="d-block w-100"
                  style="object-fit: cover"
                />
                <div
                  class="position-absolute top-0 w-100 h-100 d-flex justify-content-center align-items-center"
                  style="z-index: 4"
                >
                  <a
                    href="https://goo.gl/maps/Sgi1cR8YkqkbwZaY8"
                    target="_blank"
                  >
                    <button
                      type="button"
                      class="btn btn-outline-light"
                      @mouseover="isHovered = true"
                      @mouseleave="isHovered = false"
                    >
                      <img
                        :src="
                          isHovered
                            ? 'https://img.icons8.com/material-outlined/24/000000/marker.png'
                            : 'https://img.icons8.com/material-outlined/24/ffffff/marker.png'
                        "
                        alt="marker"
                        style="height: 24px; width: 24px"
                        loading="eager"
                      />
                      Google Maps
                    </button>
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isHovered: false,
    };
  },
  mounted() {},
};
</script>

<style>
#carousel-container {
  background: url("../assets/main-carousel-bg.png");
  background-repeat: repeat;
}

.carousel-caption > * {
  margin: 0;
  font-size: 0.8rem;
}

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
    height: 205px;
  }
}
@media (min-width: 1200px) {
  #row-parallel-with-home-carousel img {
    height: 245px;
  }
  .carousel-caption > * {
    font-size: 1rem;
  }
}
@media (min-width: 1400px) {
  #row-parallel-with-home-carousel img {
    height: 290px;
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
  z-index: 2;
  background-color: rgba(0, 0, 0, 0.35);
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

#carouselExampleAutoplaying button {
  z-index: 9;
}

.carousel-caption {
  z-index: 3;
}
</style>
