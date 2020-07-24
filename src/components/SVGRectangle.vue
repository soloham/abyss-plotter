<template>
  <rect :x="x" :y="y" :width="width" :height="height" :fill="fill" />
</template>

<script>
export default {
  name: "SVGRectangle",
  props: {
    size: Object,
    x: String,
    y: String,
    width: String,
    height: String,
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
