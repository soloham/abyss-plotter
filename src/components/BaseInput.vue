<template>
  <div id="cli-container">
    <textarea
      :value="inputCommands"
      class="cli"
      name="commands"
      cols="30"
      rows="10"
      @input="$emit('commandsUpdated', $event.target.value)"
    >
    </textarea>
  </div>
</template>

<script>
export default {
  name: "BaseInput",
  props: ["inputCommands"],
};
</script>

<style scoped>
#cli-container {
  padding: 15px;
  padding-bottom: 2px;
  padding-right: 10px;
  border-bottom-left-radius: 18px;
  border-bottom-right-radius: 18px;
  background-color: rgb(228, 245, 242);
}
.cli {
  scroll-behavior: smooth;
  border-bottom-left-radius: 18px;
  border-bottom-right-radius: 18px;
  width: 100%;
  max-width: 100%;
  min-width: 100%;
  height: 200px;
  max-height: 200px;
  min-height: 30px;
  outline: none;
  border: none;
  background-color: transparent;

  font-size: 22px;
}
</style>
