<template>
  <div class="card h-100">
    <div class="card-body"><div v-html="innerHtml"></div></div>
  </div>
</template>

<script>
export default {
  props: {
    innerHtml: {
      type: String,
    },
    heightSize: {
      type: String,
    },
  },
};
</script>

<style></style>
