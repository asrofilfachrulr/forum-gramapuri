/* eslint-disable */
<template>
  <div id="navbar-container" class="container-fluid m-0 p-0">
    <nav class="navbar navbar-expand-lg shadow-md">
      <div class="container-md">
        <a class="navbar-brand d-flex flex-nowrap" href="#">
          <img
            src="https://www.gramapuripersada.com/wp-content/uploads/2020/06/LOGO-GRAMAPURI-SOSMED-100x100.jpg"
            alt="Logo Gramapuri Persada"
            width="40"
            height="40"
            class="d-inline-block align-text-top me-2"
          />
          <div class="d-flex flex-column">
            <span class="lh-1" style="font-size: 0.85rem; letter-spacing: 2px"
              >Gramapuri Persada Blok E</span
            >
            <span class="fs-5 fw-medium">Sedekah Jum'at</span>
          </div></a
        >
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div
          class="collapse navbar-collapse justify-content-start justify-content-md-end"
          id="navbarSupportedContent"
        >
          <ul class="navbar-nav mb-2 mb-lg-0">
            <li class="nav-item ms-md-4">
              <a
                class="nav-link nav-link-top ff-condensed active"
                aria-current="page"
                href="#"
                >Tentang Kami</a
              >
            </li>
            <li class="nav-item ms-md-4">
              <a class="nav-link nav-link-top ff-condensed active" href="#"
                >Donasi</a
              >
            </li>
            <li class="nav-item ms-md-4">
              <a class="nav-link nav-link-top ff-condensed active" href="#"
                >Sambutan Ketua</a
              >
            </li>
            <li class="nav-item ms-md-4 py-2 py-md-0">
              <a class="nav-link active d-flex align-items-center" href="#">
                <img
                  width="24"
                  height="24"
                  src="https://img.icons8.com/material/24/user-male-circle--v1.png"
                  alt="user-male-circle--v1"
                />
                <span style="height: 100%" class="ps-2 ff-condensed"
                  >Masuk</span
                ></a
              >
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {};
</script>

<style>
#navbar-container {
  border-bottom: 1px solid #aeaeae;
  height: fit-content;
}

.nav-link-top {
  transition: all 300ms ease-in-out;
}

.nav-link-top:hover {
  background-color: #daecce;
  font-weight: 500;
  border-radius: 5px;
}
</style>
