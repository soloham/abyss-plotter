<template>
  <polygon :points="points" :fill="fill" />
</template>

<script>
export default {
  name: "SVGPolygon",
  props: {
    size: Object,
    points: String,
    fill: String,
  },
  data() {
    return {};
  },
};
</script>

<style scoped>
rect {
  position: absolute;
}
</style>
