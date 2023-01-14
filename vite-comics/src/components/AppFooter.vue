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
};
</script>

<template>
  <footer>
    <div class="top-footer">
      <div class="container">
        <div class="col">
          <div v-for="(object, index) in icone" :key="index">
            <a :href="object.url" :class="object.active ? 'active' : ''">
              <img :src="`/img/${object.label}`" alt="logo" />
              <span>{{ object.description }}</span>
            </a>
          </div>
        </div>
      </div>
    </div>
    <div class="main-footer">
      <div class="container">
        <div class="footer-sx">
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
            <h4>Dc</h4>
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
            <h4>Sites</h4>
            <ul>
              <li><a href="#">DC</a></li>
              <li><a href="#">MAD Magazine</a></li>
              <li><a href="#">DC Kids</a></li>
              <li><a href="#">DC Universe</a></li>
              <li><a href="#">DC Power Visa</a></li>
            </ul>
          </div>
        </div>
        <!--* <div class="dc_bg">
          <img src="/img/dc-logo-bg.png" alt="dc_logo" />
        </div> -->
      </div>
    </div>

    <!--*  <div class="social">
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

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

/* Header footer (parte bg_blue) */
.top-footer {
  background-color: $primary;
  padding: 1em 0;
  .col {
    width: 100%;
    @include d-flex-cent;
    justify-content: space-around;

    img {
      width: 50px;
      padding: 10px;
      vertical-align: middle;
    }

    span {
      color: white;
    }
  }
}

/* Main Footer Section */
.main-footer {
  background-image: url("/img/footer-bg.jpg");
  background-size: cover;

  .container {
    display: flex;
    background-image: url("/img/dc-logo-bg.png");
    background-position: center;
    background-repeat: no-repeat;
    .footer-sx {
      display: flex;
      width: 30%;
    }
    .footer-links {
      color: white;
      margin: 2em 0.6em;

      h4 {
        text-transform: uppercase;
      }

      ul {
        list-style: none;
        padding-bottom: 10px;
        li{
          padding: 5px 0;
          a{
            color:grey;
            font-size: 15px;
          }
        } 
      }
    }
  }
}

</style> 