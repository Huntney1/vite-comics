<script>
export default {
  name: "AppHeader",
  data() {
    return {
      /* lista voci nav-bar */
      menu: [
        {
          label: "CHARACTERS",
          url: "#",
          active: false,
        },
        {
          label: "COMICS",
          url: "#",
          active: true,
        },
        {
          label: "MOVIES",
          url: "#",
          active: false,
        },
        {
          label: "TV",
          url: "#",
          active: false,
        },
        {
          label: "GAMES",
          url: "#",
          active: false,
        },
        {
          label: "COLLECTIBLES",
          url: "#",
          active: false,
        },
        {
          label: "VIDEOS",
          url: "#",
          active: false,
        },
        {
          label: "FANS",
          url: "#",
          active: false,
        },
        {
          label: "NEWS",
          url: "#",
          active: false,
        },
        {
          label: "SHOP",
          url: "#",
          active: false,
        },
      ],
    };
  },
};
</script>


<template>
  <header>
    <div class="continer">
      <!-- logo dc -->
      <a href="/" class="logo">
        <img src="../assets/vue-dc-comics-1/img/dc-logo.png" alt="logo_dc" />
      </a>
      <!-- attivo lista nav bar -->
      <nav>
        <ul>
          <li v-for="(item, index) in menu" :key="index"  >
            <a :href="item.url" :class="item.active ? 'active' : ''"></a>
            {{ item.label }}
          </li>
        </ul>
      </nav>
    </div>
    <div class="content_cont">
        <div class="contet_title">  ...content goes here ...  </div>
    </div>
  </header>
</template>

<style lang="scss" scope>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;
@use "../styles/partials/generals" as *;

header {
  text-align: center;

  img {
    width: 50px;
    margin-top: 14px;
  }

  div {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
  }

  ul {
    @include display-flex-sb;
    margin: 25px 10px;
    list-style: none;

    
}

li a{
    margin: 6px;
    line-height: 1px;
    text-decoration: none;
    transition: border 0.3s;
    
    &.active, &:hover{
        color: blue;
        border-bottom: 4px solid blue;
    }
}

.content_cont {
    height: 100px;
    background-color: rgb(36, 34, 34);
    display: flex;
    align-items: center;


    .contet_title {
        color: white;
       
    }
}


}
</style>