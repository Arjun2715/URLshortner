<script setup>
import NavBarVue from "./components/NavBar.vue";
import card from "./components/card.vue";
import FooterVue from "./components/Footer.vue";
</script>
<template>
  <div class="overflow-y-hidden">
    <NavBarVue />
    <div class="flex justify-center my-40">
      <card />
    </div>
    <FooterVue />
  </div>
</template>
