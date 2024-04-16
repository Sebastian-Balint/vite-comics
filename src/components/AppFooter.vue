<script>
export default {
  name: "AppFooter",
  data() {
    return {
      links: [
        {
          mainText: "DC COMICS",
          text: [
            {
              lower: "Characters",
            },
            {
              lower: "Comics",
            },
            {
              lower: "Movies",
            },
            {
              lower: "TV",
            },
            {
              lower: "Games",
            },
            {
              lower: "Videos",
            },
            {
              lower: "News",
            },
          ],
        },
        {
          mainText: "SHOP",
          text: [
            {
              lower: "Shop DC",
            },
            {
              lower: "Shop DC Collectibles",
            },
          ],
        },
        {
          mainText: "DC",
          text: [
            {
              lower: "Terms Of Use",
            },
            {
              lower: "Privacy policy (New)",
            },
            {
              lower: "Ad Choices",
            },
            {
              lower: "Advertising",
            },
            {
              lower: "Jobs",
            },
            {
              lower: "Subscriptions",
            },
            {
              lower: "Talent Workshops",
            },
            {
              lower: "CPSC Certificates",
            },
            {
              lower: "Ratings",
            },
            {
              lower: "Shop Help",
            },
            {
              lower: "Contact Us",
            },
          ],
        },
        {
          mainText: "SITES",
          text: [
            {
              lower: "DC",
            },
            {
              lower: "MAD Magazine",
            },
            {
              lower: "DC Kids",
            },
            {
              lower: "DC Universe",
            },
            {
              lower: "DC Power Visa",
            },
          ],
        },
      ],
      images: [
        {
          image: "footer-facebook.png",
        },
        {
          image: "footer-twitter.png",
        },
        {
          image: "footer-youtube.png",
        },
        {
          image: "footer-pinterest.png",
        },
        {
          image: "footer-periscope.png",
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
  <footer>
    <div class="container">
      <div class="jumbo">
        <img src="../assets/img/dc-logo-bg.png" alt="" />
        <div class="container-link" v-for="link in links">
          <h2>{{ link.mainText }}</h2>
          <ul>
            <li v-for="text in link.text">{{ text.lower }}</li>
          </ul>
        </div>
      </div>
      <div class="bottom">
        <div class="container-bottom">
          <button class="btn">SIGN-UP NOW!</button>
          <div class="social">
            <h1>FOLLOW US</h1>
            <li v-for="image in images">
              <img :src="getImage(image.image)" alt="" />
            </li>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;
.container {
  .jumbo {
    background-image: url(./../assets/img/footer-bg.jpg);
    background-size: cover;
    height: 340px;
    position: relative;
    overflow: hidden;
    img {
      position: absolute;
      right: 200px;
      bottom: -100px;
    }
    .container-link {
      margin: 0 auto;
      max-width: 1000px;
      display: flex;
      flex-direction: column;
      flex-wrap: wrap;
      color: white;
    }
  }
  .bottom {
    min-height: 100px;
    background-color: #303030;
    .container-bottom {
      max-width: 1000px;
      margin: 0 auto;
      padding: 30px;
      display: flex;
      justify-content: space-between;

      .btn {
        border: 1px solid $brand-primary;
        background-color: #303030;
        color: white;
        padding: 14px;
      }
      .social {
        display: flex;
        align-items: center;
        color: $brand-primary;
        h1 {
          font-size: 20px;
        }
        li {
          padding: 0 10px;
        }
      }
    }
  }
}
</style>
