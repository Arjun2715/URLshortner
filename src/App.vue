<script setup>
import NavBarVue from "./components/NavBar.vue";
import card from "./components/card.vue";
import FooterVue from "./components/Footer.vue";
// import info from "./components/info.vue";

// export default {
//   components: {

//   },

// };
</script>
<template>
  <div class="overflow-y-hidden">
    <NavBarVue />
    <div class="flex justify-center my-40">
      <card />
    </div>
    <!-- <div class="flex justify-center">
      <info />

    </div> -->
    <FooterVue />
  </div>
</template>