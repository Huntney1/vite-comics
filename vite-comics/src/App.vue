<script>
import AppHeader from "./components/AppHeader.vue";
import AppFooter from "./components/AppFooter.vue";
/* import Appjumbotron from "./components/Appjumbotron.vue"; */

export default {
  components: {
    AppHeader,
   /*  Appjumbotron, */
    AppFooter,
  },
};
</script>

<template>
  <div>
    <AppHeader />
    <!-- <Appjumbotron /> -->
    <AppFooter />
  </div>
</template>


<style lang="scss">
@use "./styles/generals.scss" as *;
</style>
