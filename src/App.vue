<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> 
  msg="Welcome to Your Vue.js App"-->
  <UrlShortner />  
</template>

<script>
import UrlShortner from './components/UrlShortner.vue'

export default {
  name: 'App',
  components: {
    UrlShortner
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
