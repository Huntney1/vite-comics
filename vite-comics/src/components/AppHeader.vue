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
  <header class="continer">
    <div >
      <!-- logo dc -->
      <a href="/" class="logo">
        <img src="/img/dc-logo.png" alt="logo_dc" />
      </a>
      <!-- attivo lista nav bar -->
      <nav>
        <ul>
          <li v-for="(item, index) in menu" :key="index">
            <a :href="item.url" :class="item.active ? 'active' : ''"></a>
            {{ item.label }}
          </li>
        </ul>
      </nav>
    </div>
    <div class="content_cont">
      <div class="contet_title">...content goes here ...</div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;


header {
  text-align: center;

  img {
    width: 50px;
    margin-top: 14px;
  }

  div {
    @include d-flex-bt;
    align-items: center;
  }

  ul {
    @include display-flex-sb;
    margin: 25px 10px;
    list-style: none;
  }

  li a {
    margin: 6px;
    line-height: 1px;
   
    border-bottom: 3px solid white;
  }
  li.active,
  li:hover {
    color: $primary;
    border-bottom: 3px solid $primary;
    cursor: pointer;
  }

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
}
</style>