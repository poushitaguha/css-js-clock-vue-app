<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Poushita msg="Welcome to Poushita's Vue Component"/>
    <PerrysComponent msg="Perry's clock"/>
  </div>
</template>

<script>
import Poushita from "./components/Poushita.vue";
import PerrysComponent from "./components/PerrysComponent.vue";

export default {
  name: "app",
  components: {
    Poushita,
    PerrysComponent
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
}
html {
  background: #018ded url(http://unsplash.it/1500/1000?image=881&blur=50);
  background-size: cover;
  font-family: "Helvetica Neue";
  text-align: center;
  font-size: 10px;
}

body {
  font-size: 2rem;
  display: flex;
  flex: 1;
  min-height: 100vh;
  align-items: center;
  justify-content: center;
}
</style>
