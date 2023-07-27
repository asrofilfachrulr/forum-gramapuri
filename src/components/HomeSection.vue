<template>
  <div
    class="container-fluid p-0 m-0 my-4"
    :style="shade.state ? shade.css : ''"
  >
    <component :is="innerComponent"></component>
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
};
</script>

<style></style>
