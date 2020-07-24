<template>
  <div>
    <h1 id="title">Abyss Plotter</h1>
    <div id="nav">
      <router-link to="/">Try</router-link>
      <router-link to="/usage">Usage</router-link>
      <router-link to="/examples">Examples</router-link>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
#title {
  font-size: 60px;
  margin: 20px;
}
#nav {
  padding: 0px;
}

#nav a {
  font-size: 27px;
  font-weight: bold;
  color: #2c3e50;

  text-decoration: none;
  padding: 0 10px;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
