<script>
import comicsData from "../assets/data/dc-comics.json";
import AppJumbotron from "./AppJumbotron.vue";
export default {
  name: "AppContent",
  AppJumbotron,
  data() {
    return {
      comics: comicsData,
    };
  },
};
</script>

<template lang="">
    <AppJumbotron />
    <div class="dark">
      <div class="container">
        <div class="upper-title">
          <h2 class="title">
            Comics Series
          </h2>
        </div>
      </div>
      <div class="container">
        <div class="comics-container">
          <dvi class="comics-card" v-for="(comics, index) in comics":key="index" >
            <div class="thumb-container">
              <img :src="comic.thumb" class="thumb" :alt="comic.series">
              <h4>{{comic.series}}</h4>
            </div>
          </dvi>
            </div>
      </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.dark {
  background-color: black;
}

.upper-title{
  position: relative;


.title{
  width: 250px;
  text-transform: uppercase;
  background-color: $primary;
  padding: 15px;
  text-align: center;
  color:white;
  position:absolute;
  top: -25px;
  border: 1px solid black;
}
}

</style>