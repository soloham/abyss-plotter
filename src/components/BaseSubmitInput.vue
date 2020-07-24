<template>
  <div>
    <input type="submit" value="PLOT" @click="$emit('submitted')" />
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
div {
  margin: auto;
  width: 450px;
}

input[type="submit"] {
  width: 70%;
  height: 55px;

  border: none;
  outline: none;
  border-radius: 15px;

  font-weight: bold;
  font-size: 22px;

  cursor: pointer;

  background-color: rgba(224, 236, 238, 0.746);
  color: #2c3e50;
}

input[type="submit"]:hover {
  background-color: rgba(216, 227, 230, 0.746);
}

input[type="submit"]:active {
  background-color: rgba(203, 214, 218, 0.746);
}
</style>
