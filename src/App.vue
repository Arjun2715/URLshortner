<script setup>
import NavBarVue from "./components/NavBar.vue";
import card from "./components/card.vue";
import FooterVue from "./components/Footer.vue";


</script>

<template>
  <div class="">
    <NavBarVue />
    <div class="flex justify-center  my-40">
      <card />
    </div>
    <FooterVue />
  </div>
  
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>

    <!-- <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  <HelloWorld msg="Vite + Vue" /> -->