<template>
  <div
    class="modal fade"
    id="basic-info-modal"
    tabindex="-1"
    aria-hidden="true"
    :data-bs-backdrop="data.isStatic ? 'static' : true"
  >
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content">
        <div class="modal-header">
          <h1 class="modal-title fs-5">
            {{ data.title }}
          </h1>
        </div>
        <div class="modal-body">{{ data.message }}</div>
        <div class="modal-footer">
          <button
            type="button"
            :class="'btn btn-' + data.buttonStyle"
            data-bs-dismiss="modal"
          >
            {{ data.buttonText }}
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    dataProp: {
      type: Object,
      default: () => {
        return {};
      },
    },
    typeInfo: {
      type: String, // "maintenance", "custom", ... <to be added soon>
    },
  },
  data() {
    return {
      data: {},
      isShow: false,
      defaultData: {
        title: "Informasi",
        message: "Pesan",
        buttonText: "Tutup",
        buttonStyle: "primary",
        isStatic: false,
      },
      maintenanceData: {
        title: "Informasi",
        message: "Fitur ini masih dalam pengembangan. Terimakasih.",
        buttonText: "Tutup",
        buttonStyle: "primary",
        isStatic: false,
      },
    };
  },
  methods: {
    observeModalShow() {
      const modal = document.getElementById("basic-info-modal");
      const observer = new MutationObserver(() => {
        this.isShow = modal.classList.contains("show");
      });

      observer.observe(modal, { attributes: true, attributeFilter: ["class"] });
    },
  },
  mounted() {
    this.observeModalShow();
    this.data = this.defaultData;
  },
  watch: {
    isShow(state) {
      if (state) {
        this.data = this.typeInfo ? this.maintenanceData : this.data;
      } else {
        this.data = this.defaultData;
      }
    },
  },
};
</script>

<style>
.btn-primary {
  --bs-btn-color: #fff;
  --bs-btn-bg: var(--clr-accent);
  --bs-btn-border-color: var(--clr-accent);
  --bs-btn-hover-color: #fff;
  --bs-btn-hover-bg: var(--clr-accent-dark);
  --bs-btn-hover-border-color: var(--clr-accent-dark);
  --bs-btn-focus-shadow-rgb: 49, 132, 253;
  --bs-btn-active-color: #fff;
  --bs-btn-active-bg: var(--clr-accent-dark);
  --bs-btn-active-border-color: var(--clr-accent-dark);
  --bs-btn-active-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  --bs-btn-disabled-color: #fff;
  --bs-btn-disabled-bg: var(--clr-accent-light);
  --bs-btn-disabled-border-color: var(--clr-accent-light);
}
</style>
