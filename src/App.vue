<template>
  <div id="app">
    <img alt="vue" src="./assets/logo.png" id="logo">
    <Slide/>
  </div>
</template>

<script>
import Slide from './components/Slide.vue'
export default {
  name: 'app',
  components: {
    Slide
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000;
}

body{
  background-color: #000;
}

</style>
