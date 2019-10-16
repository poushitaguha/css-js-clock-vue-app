<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Poushita msg="Welcome to Poushita's Vue Component"/>
  </div>
</template>

<script>
import Poushita from "./components/Poushita.vue";

export default {
  name: "app",
  components: {
    Poushita
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
