<template>
  <div id="app">
    <Header />
    <keep-alive>
      <router-view />
    </keep-alive>
  </div>
</template>

<script>
import Header from "./components/Header";

export default {
  name: "App",
  components: {
    Header,
  },
};
</script>

<style>
body {
  height: 100vh;

  display: flex;
  flex-direction: column;
  justify-content: center;

  text-align: center;
  margin: 0;
}

#app {
  font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
    "Lucida Sans", Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
