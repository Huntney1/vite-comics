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
    <!-- NavBar -->
    <div class="navbar">
      <!-- logo dc -->
      <a href="#" class="logo">
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
  </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.navbar {
  @include d-flex-sb;
  height: 150px;
  align-items: center;
  margin: 1em 0;

  nav {
    @include d-flex-cent;
    height: 100%;

    ul {
      height: 100%;
      display: flex;
      list-style: none;

      li {
        @include d-flex-cent;
        height: 100%;
        padding: 10px;
        line-height: 1px;
        border-bottom: 3px solid white;
        transition: border 0.3s;
        &.active {
          /* color: $primary; */
          border-bottom: $primary;
          cursor: pointer;

          a {
            color: $primary;
          }
        }
        a:hover {
          border-bottom: $primary;
        }
      }
    }
  }
}
</style>