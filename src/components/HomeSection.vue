<template>
  <div
    class="container-fluid p-0 m-0 my-4"
    :style="shade.state ? 'background-color: ' + shade.color : ''"
  >
    <component
      :is="innerComponent"
      @modal-type-info="emitModalTypeInfo"
    ></component>
  </div>
</template>

<script>
export default {
  props: {
    innerComponent: {
      type: Object,
    },
    shade: {
      default: () => {
        return { state: false };
      },
      type: Object,
    },
  },
  methods: {
    emitModalTypeInfo(value) {
      console.log(
        "emitted modal-type-info from Home Section with value",
        value
      );
      this.$emit("modal-type-info", value);
    },
  },
};
</script>

<style></style>
