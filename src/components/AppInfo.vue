<script>
export default {
  name: "AppInfo",
  data() {
    return {
      links: [
        {
          image: "buy-comics-digital-comics.png",
          text: "DIGITAL COMICS",
        },
        {
          image: "buy-comics-merchandise.png",
          text: "DC MERCHANDISE",
        },
        {
          image: "buy-comics-subscriptions.png",
          text: "SUBSCRIPTION",
        },
        {
          image: "buy-comics-shop-locator.png",
          text: "COMIC SHOP LOCATOR",
        },
        {
          image: "buy-dc-power-visa.svg",
          text: "DC POWER VISA",
        },
      ],
    };
  },
  methods: {
    getImage(name) {
      return new URL(`../assets/img/${name}`, import.meta.url).href;
    },
  },
};
</script>
<template>
  <div class="container">
    <div class="container-info">
      <div class="links" v-for="link in links">
        <div class="link-img"><img :src="getImage(link.image)" alt="" /></div>
        <div class="link-text">{{ link.text }}</div>
      </div>
    </div>
  </div>
</template>
<style scoped lang="scss">
@use "../style/partials/-variables" as *;
.container {
  background-color: $brand-primary;

  .container-info {
    display: flex;
    margin: 0 auto;
    max-width: 1000px;
    .links {
      display: flex;
      align-items: center;

      margin: 30px auto;

      &:nth-child(4) {
        img {
          width: 36px;
        }
      }
    }

    .link-img {
      img {
        width: 50px;
        margin-right: 6px;
      }
    }
    .link-text {
      color: white;
      font-size: 12px;
    }
  }
}
</style>
