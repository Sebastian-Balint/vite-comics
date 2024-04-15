<script>
export default {
  name: "AppHeader",
  data() {
    return {
      links: [
        {
          text: "CHARACTERC",
          active: false,
        },
        {
          text: "COMICS",
          active: false,
        },
        {
          text: "MOVIES",
          active: false,
        },
        {
          text: "TV",
          active: false,
        },
        {
          text: "GAMES",
          active: false,
        },
        {
          text: "COLLECTIBLES",
          active: false,
        },
        {
          text: "VIDEOS",
          active: false,
        },
        {
          text: "FANS",
          active: false,
        },
        {
          text: "NEWS",
          active: false,
        },
        {
          text: "SHOP",
          active: false,
        },
      ],
      activeItem: 0,
    };
  },
  methods: {
    showActiveNav(index) {
      this.activeItem = index;
    },
  },
};
</script>

<template>
  <header>
    <div class="container">
      <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="" />
      </div>
      <nav>
        <ul>
          <li
            :class="{ 'active': activeItem === index }"
            v-for="(link, index) in links"
            @click="showActiveNav(index)"
          >
            <a href="#">{{ link.text }}</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style scoped lang="scss">
@use "../style/partials/-variables" as *;
.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1000px;
  margin: 0 auto;
}
.logo img {
  width: 70px;
  margin: 14px 0;
}
nav {
  ul {
    display: flex;
  }
  li {
    padding: 40px 8px;
    text-decoration: none;
    font-size: 14px;
    color: black;
    &.active {
      border-bottom: 5px solid $brand-primary;
      a {
        color: $brand-primary;
      }
    }
  }
}
</style>
