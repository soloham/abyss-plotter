<template>
  <div>
    <div id="main-container">
      <BaseInput :inputCommands="commands" @commandsUpdated="updateCommands" />
      <Plot :commandsList="commandsList" />
    </div>

    <BaseSubmitInput @submitted="commandsList = commands.split('\n')" />
  </div>
</template>

<script>
import BaseInput from "../components/BaseInput";
import BaseSubmitInput from "../components/BaseSubmitInput";

import Plot from "../components/Plot";

export default {
  name: "Main",
  components: { BaseInput, BaseSubmitInput, Plot },
  methods: {
    updateCommands(commands) {
      this.commands = commands;
    },
  },
  data() {
    return {
      commands: `p 200,10 250,190 160,200 
c 25 100 20 
r 100 50 25 25
r 10 150 70 70
c 80 220 20

pl 0,250 250,250 250,0 0,0 0,250`,
      commandsList: [],
    };
  },
};
</script>

<style scoped>
#main-container {
  width: 450px;
  height: 500px;

  background: rgb(240, 246, 246);
  border-radius: 10%;

  margin: 40px auto;

  display: flex;
  flex-direction: column-reverse;
}
</style>
