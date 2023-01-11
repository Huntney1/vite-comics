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
    <!-- logo dc -->
    <a href="/" class="logo">
      <img src="../assets/vue-dc-comics-1/img/dc-logo.png" alt="logo_dc" />
    </a>
    <!-- attivo lista nav bar -->
    <nav>
      <ul>
        <li v-for="(item, index) in menu" :key="index">
          <a :href="item.url" class="item.active ? 'active' : ''"></a>
          {{ item.label }}
        </li>
      </ul>
    </nav>
  </header>
</template>