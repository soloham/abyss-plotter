<template>
  <polyline
    :points="points"
    style="fill:transparent;stroke-width:3"
    :stroke="fill"
  />
</template>

<script>
export default {
  name: "SVGPolyline",
  props: {
    size: Object,
    points: String,
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
