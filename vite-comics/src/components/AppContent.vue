<script>
export default {
  name: "AppContent",
  data() {
    return {
      
     
    };
  },
};
</script>


<template>
    <div class="content_cont">
      <div class="contet_title">...content goes here ...</div>
    </div>
</template>

<style lang="scss" scope>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;
@use "../styles/partials/generals" as *;


.content_cont {
    height: 100px;
    margin-top: 5px;
    background-color: rgb(36, 34, 34);
    display: flex;
    align-items: center;

    .contet_title {
      color: white;
      text-transform: uppercase;
    }
  }


</style>