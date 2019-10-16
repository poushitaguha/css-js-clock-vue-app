<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
<<<<<<< Updated upstream
    <Poushita msg="Welcome to Poushita's Vue Component"/>
=======
    <PerrysComponent msg="Perry's clock"/>
>>>>>>> Stashed changes
  </div>
</template>

<script>
<<<<<<< Updated upstream
import Poushita from "./components/Poushita.vue";
=======
import PerrysComponent from './components/PerrysComponent.vue';
>>>>>>> Stashed changes

export default {
  name: "app",
  components: {
<<<<<<< Updated upstream
    Poushita
=======
    PerrysComponent
>>>>>>> Stashed changes
  }
};
</script>

<style>
<<<<<<< Updated upstream
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
=======
html {
    background: #018DED url(http://unsplash.it/1500/1000?image=881&blur=50);
    background-size: cover;
    font-family: 'Helvetica Neue';
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

/* #app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
>>>>>>> Stashed changes
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
