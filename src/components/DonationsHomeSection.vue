<template>
  <div class="container py-5">
    <div class="row justify-content-center">
      <div
        class="col-12 col-md-12 col-lg-6 d-flex justify-content-center mb-5 mb-lg-0"
      >
        <div id="donation" class="my-lg-auto" style="width: fit-content">
          <h1 class="underline-accent ff-condensed text-center pb-3">
            Ayo Donasi!
          </h1>
        </div>
      </div>
      <div class="col-12 col-md-6 col-lg-6 px-4 px-md-0">
        <div class="row">
          <ul class="nav nav-pills">
            <li class="nav-item">
              <a
                class="nav-link fw-bold active"
                data-bs-toggle="tab"
                href="#donation-card-1"
                role="tab"
                aria-current="page"
                >Bank Mandiri</a
              >
            </li>
            <li class="nav-item">
              <a
                class="nav-link fw-bold"
                data-bs-toggle="tab"
                href="#donation-card-2"
                role="tab"
                >Bank BNI</a
              >
            </li>
          </ul>
        </div>
        <div class="row">
          <div class="tab-content p-0 mt-3">
            <div
              class="tab-pane fade show active"
              id="donation-card-1"
              role="tabpanel"
            >
              <!-- Card 1 content -->
              <div class="card">
                <div class="card-body" style="height: 160px">
                  <h5 class="card-title fw-bold">1520001245</h5>
                  <p class="card-text">
                    <span>a.n Aisyah</span
                    ><img
                      style="height: 100%; width: auto"
                      class="float-end"
                      src="../assets/bank-mandiri.png"
                      alt="logo-bank-mandiri"
                    />
                  </p>
                </div>
              </div>
            </div>
            <div class="tab-pane fade" id="donation-card-2" role="tabpanel">
              <!-- Card 2 content -->
              <div class="card">
                <div class="card-body" style="height: 160px">
                  <h5 class="card-title">52000012</h5>
                  <p class="card-text d-flex justify-content-between">
                    <span>a.n Rina Aulia</span
                    ><img
                      style="height: 100%; width: auto"
                      class="float-end"
                      src="../assets/bank-bni.png"
                      alt="logo-bank-bni"
                    />
                  </p>
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
export default {};
</script>

<style>
.nav-pills .nav-link.active,
.nav-pills .show > .nav-link {
  color: var(--bs-nav-pills-link-active-color);
  background-color: var(--clr-accent);
}

.nav-link {
  color: var(--clr-accent);
}
</style>
