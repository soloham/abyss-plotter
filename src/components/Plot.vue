<template>
  <div id="plot-container">
    <svg :height="size.height" :width="size.width">
      <template v-for="(command, i) in commandsList">
        <template v-if="regRect.test(command)">
          <SVGRectangle
            :key="i"
            :size="size"
            :x="command.split(/\s+/)[1]"
            :y="command.split(/\s+/)[2]"
            :height="command.split(/\s+/)[4]"
            :width="command.split(/\s+/)[3]"
            :fill="randomColour()"
          />
        </template>

        <template v-else-if="regCircle.test(command)">
          <SVGCircle
            :key="i"
            :size="size"
            :cx="command.split(/\s+/)[1]"
            :cy="command.split(/\s+/)[2]"
            :r="command.split(/\s+/)[3]"
            :fill="randomColour()"
          />
        </template>

        <template v-else-if="regPolyG.test(command)">
          <SVGPolygon
            :key="i"
            :size="size"
            :points="command.substr(1)"
            :fill="randomColour()"
          />
        </template>

        <template v-else-if="regPolyL.test(command)">
          <SVGPolyline
            :key="i"
            :size="size"
            :points="command.substr(2)"
            :fill="randomColour()"
          />
        </template>

        <template v-else-if="regBlank.test(command)"></template>
        <template v-else>{{ addError(i) }}</template>
      </template>
      {{ alert() }}
    </svg>
  </div>
</template>

<script>
import SVGRectangle from "./SVGRectangle";
import SVGCircle from "./SVGCircle";
import SVGPolygon from "./SVGPolygon";
import SVGPolyline from "./SVGPolyline";

const errors = [];
export default {
  components: {
    SVGRectangle,
    SVGCircle,
    SVGPolygon,
    SVGPolyline,
  },
  props: ["commandsList"],
  methods: {
    addError(index) {
      errors.push(index + 1);
    },
    alert() {
      if (errors.length > 0) {
        alert(`Error(s) in line: ${errors}\nPlease check the usage.`);
        errors.splice(0, errors.length);
      }
    },
    randomColour() {
      return "#" + Math.floor(Math.random() * 16777215).toString(16);
    },
  },
  data() {
    return {
      size: { height: "250", width: "250" },
      regCircle: /^[cC]\s+\d+\s+\d+\s+\d+\s*$/,
      regRect: /^[rR]\s+\d+\s+\d+\s+\d+\s+\d+\s*$/,
      regPolyG: /^[pP](\s+\d+\s*,\s*\d+\s*){3,}$/,
      regPolyL: /^[pP][lL](\s+\d+\s*,\s*\d+\s*){3,}$/,
      regBlank: /^\s*$/,
    };
  },
};
</script>

<style>
#plot-container {
  overflow: hidden;
}
</style>
