<template>
  <b-container fluid>
    <b-row class="p-0">
      <b-col class="p-0">
        <div
          class="parallax-image"
          style=" 
            overflow: hidden;"
          :style="{
            maxHeight: windowHeight - 77 + 'px'
          }"
        >
          <picture>
            <!-- <source srcset="~assets/images/home/home_splash-min.webp" type="image/webp" class="img-fluid dark-overlay"> -->
            <img
              src="/coffee_mug-matt-hoffman-unsplash.jpg"
              alt="third wave Splash page"
              class="img-fluid centered-image"
            />
          </picture>
        </div>

        <div class="splash-text rounded ">
          <h2 class="wheat-text m-3">
            your orders.
            <br />
            <span class="italic">
              ready for pick up.
            </span>
          </h2>
          <b-button variant="primary" class="sienna-text wheat-bg m-3"
            >Contact Us</b-button
          >
        </div>
        <b-card
          class="notification-text italic"
          no-body
          img-src="https://placekitten.com/380/200"
          img-alt="Image"
          img-top
        >
          <template v-slot:header>
            <h4 class="mb-0">Hello World</h4>
          </template>

          <b-card-body>
            <b-card-title>Card Title</b-card-title>
            <b-card-sub-title class="mb-2">Card Sub Title</b-card-sub-title>
            <b-card-text>
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </b-card-text>
          </b-card-body>

          <b-list-group flush>
            <b-list-group-item>Cras justo odio</b-list-group-item>
            <b-list-group-item>Dapibus ac facilisis in</b-list-group-item>
            <b-list-group-item>Vestibulum at eros</b-list-group-item>
          </b-list-group>

          <b-card-body>
            <a href="#" class="card-link">Card link</a>
            <a href="#" class="card-link">Another link</a>
          </b-card-body>

          <b-card-footer>This is a footer</b-card-footer>

          <b-card-img
            src="https://placekitten.com/480/210"
            alt="Image"
            bottom
          ></b-card-img>
        </b-card>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      windowHeight: null,
      windowWidth: null,
      backgroundURL:
        "url('/coffee_mug-matt-hoffman-unsplash.jpg') no-repeat center fixed"
    }
  },
  mounted() {
    this.windowHeight = window.innerHeight
    this.windowWidth = window.innerWidth
  }
}
</script>

<style lang="scss">
$break-small: 600px;
$break-large: 1000px;
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;1,700&display=swap');
.btn-primary:hover,
.btn-primary:focus,
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: wheat !important;
  background-color: sienna !important;
  border-color: sienna !important;
}

.btn-primary {
  border-color: wheat !important;
}

.sienna-text {
  color: sienna;
}

.wheat-text {
  color: wheat;
}

.wheat-bg {
  background-color: wheat;
}

.italic {
  font-style: italic;
}

.splash-text {
  z-index: 2;
  position: absolute;
  top: 15%;
  left: 15%;
  @media screen and (max-width: $break-large) {
    position: relative;
    // // min-height: 100%;
    // // min-width: 100%;
    top: initial;
    left: initial;
    transform: none;
    background-color: sienna;
  }
}

.notification-text {
  z-index: 2;
  position: absolute;
  top: 15%;
  left: 75%;
  max-width: 20%;
  @media screen and (max-width: $break-large) {
    position: relative;
    // // min-height: 100%;
    // // min-width: 100%;
    top: initial;
    left: initial;
    transform: none;
    background-color: sienna;
  }
}

.centered-image {
  // position: relative;
  // top: 50%;
  // transform: translate(0%, -17.5%);
  @media screen and (max-width: $break-large) {
    display: none;
  }
}
</style>
