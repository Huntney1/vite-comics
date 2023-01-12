<script>
export default {
  name: "AppFooter",
  data() {
    return {
      icone: [
        {
          label: "buy-comics-digital-comics.png",
          active: false,
          description: "DIGITAL COMICS",
        },
        {
          label: "buy-comics-merchandise.png",
          active: true,
          description: "DC MERCHANDISE",
        },
        {
          label: "buy-comics-subscriptions.png",
          active: false,
          description: "SUBSCRIPTION",
        },
        {
          label: "buy-comics-shop-locator.png",
          active: false,
          description: "COMIC SHOP LOCATOR",
        },
        {
          label: "buy-dc-power-visa.svg",
          active: false,
          description: "DC POWER VISA",
        },
      ],
      social: [
        {
          logo: "footer-facebook.png",
        },
        {
          logo: "footer-periscope.png",
        },
        {
          logo: "footer-pinterest.png",
        },
        {
          logo: "footer-twitter.png",
        },
        {
          logo: "footer-youtube.png",
        },
      ],
    };
  },
 /* methods: {
    getImagePath: function (img) {
      return `../assets/vue-dc-comics-1/img${img}`;
    },
  },*/
};
</script>


<template>
  <footer>
    <div class="footer-section">
      <div class="container">
        <ul>
          <li v-for="(object, index) in icone" :key="index">
            <a :href="object.url" :class="object.active ? 'active' : ''">
              <img :src="`/img/${object.label}`" alt="logo" />
              <span>{{ object.description }}</span>
            </a>
          </li>
        </ul>
      </div>
    </div>

    <div class="cols cont_list">
      <div class="footer-links">
        <h4>Dc Comics</h4>
        <ul>
          <li><a href="#">Characters</a></li>
          <li><a href="#">Comics</a></li>
          <li><a href="#">Movies</a></li>
          <li><a href="#">TV</a></li>
          <li><a href="#">Games</a></li>
          <li><a href="#">Videos</a></li>
          <li><a href="#">News</a></li>
        </ul>
      </div>

      <div class="footer-links">
        <h4>Shop</h4>
        <ul>
          <li><a href="#">Shop DC</a></li>
          <li><a href="#">Shop DC Collectibles</a></li>
        </ul>
      </div>

      <div class="footer-links">
        <h4>DC</h4>
        <ul>
          <li><a href="#">Temos Of Use</a></li>
          <li><a href="#">Privacy policy (New)</a></li>
          <li><a href="#">Ad Choices</a></li>
          <li><a href="#">Advertising</a></li>
          <li><a href="#">Jobs</a></li>
          <li><a href="#">Subscriptions</a></li>
          <li><a href="#">Talent Workshops</a></li>
          <li><a href="#">CPSC Cerrificates</a></li>
          <li><a href="#">Ratings</a></li>
          <li><a href="#">Shop Help</a></li>
          <li><a href="#">Contact Us</a></li>
        </ul>
      </div>

      <div class="footer-links">
        <h4>SITES</h4>
        <ul>
          <li><a href="#">DC</a></li>
          <li><a href="#">MAD Magazine</a></li>
          <li><a href="#">DC Kids</a></li>
          <li><a href="#">DC Universe</a></li>
          <li><a href="#">DC Power Visa</a></li>
        </ul>
      </div>

      <div class="dc_bg">
        <img src="../assets/vue-dc-comics-1/img/dc-logo-bg.png" alt="dc_logo" />
      </div>
    </div>

   <!--  <div class="social">
      <div class="col-but">
        <button class="footer-button">Sign-up now!</button>
      </div>
      <div class="icon">
        <h3 class="follow">Follow us</h3>
        <ul>
          <li v-for="(object, index) in social" :key="index">
            <a href="#"><img :src="getImagePath(object.logo)" alt="loghi" /></a>
          </li>
        </ul>
      </div>
    </div> -->
  </footer>
</template>

<style lang="scss" scope>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.footer-bar {
  padding: 2em 5em;
  background-color: #0282f9;
  width: 100%;
}

.link-flex {
  display: flex;
  align-items: center;
}
</style> 