<script>
import comicsData from "../assets/data/dc-comics.json";
import Jumbotron from "./Jumbotron.vue";
import ComicCard from "./ComicCard.vue";

export default {
  name: "ComicsList",
  components:{
    Jumbotron,
    ComicCard
  },
  data() {
    return {
      comics: comicsData,
    };
  },
};
</script>

<template lang="">
  <Jumbotron />
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
          <ComicCard v-for="(item, index) in comics" :key="index" :comic="item"/>
        </div>
      </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.dark {
  background-color: rgb(30, 30, 30);
}

.upper-title {
  position: relative;

  .title {
    width: 250px;
    text-transform: uppercase;
    background-color: $primary;
    padding: 15px;
    text-align: center;
    color: white;
    position: absolute;
    top: -25px;
    border: 1px solid black;
  }
}

.comics-container{
   @include d-flex-sb;
  align-items: center;
  flex-wrap: wrap;

}
</style>