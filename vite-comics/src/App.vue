<script>
import AppHeader from "./components/AppHeader.vue";
import AppJumbotron from "./components/Jumbotron.vue";
import ComicsList from "./components/ComicsList.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  components: {
    AppHeader,
    AppJumbotron,
    ComicsList,
    AppFooter,
  },
};
</script>

<template>
  <div>
    <AppHeader />
    <AppJumbotron />
    <ComicsList />
    <AppFooter />
  </div>
</template>


<style lang="scss">
@use "./styles/generals.scss" as *;
</style>
