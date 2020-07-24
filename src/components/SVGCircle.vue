<template>
  <circle :cx="cx" :cy="cy" :r="r" :fill="fill" />
</template>

<script>
export default {
  name: "SVGCircle",
  props: {
    size: Object,
    cx: String,
    cy: String,
    r: String,
    fill: String,
  },
  data() {
    return {
      
    };
  },
};
</script>

<style scoped>
rect {
  position: absolute;
}
</style>
