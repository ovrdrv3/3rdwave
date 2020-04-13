<template>
  <div>
    <b-nav :vertical="narrowDevice">
      <b-nav-item active>3rdwave</b-nav-item>
      <b-nav-item>what we do</b-nav-item>
      <b-nav-item>pricing</b-nav-item>
      <b-nav-item>contact us</b-nav-item>
    </b-nav>
    <div
      id="centerCallToAction"
      class="wheat-text"
      :style="{
        top: windowHeight / 2 - 50 + 'px',
        left: windowWidth / 2 - 130 + 'px'
      }"
      style="position: absolute;"
    >
      <h2>
        your orders.
        <br />
        <span class="italic">
          ready for pick up.
        </span>
      </h2>
      <b-button variant="primary" class="sienna-text wheat-bg"
        >Contact Us</b-button
      >
    </div>
  </div>
  <!-- </div> -->
</template>

<script>
export default {
  components: {},
  data() {
    return {
      windowHeight: null,
      windowWidth: null
    }
  },
  computed: {
    narrowDevice() {
      return this.windowWidth <= 576
    }
  },
  mounted() {
    this.windowHeight = window.innerHeight
    this.windowWidth = window.innerWidth
  }
}
</script>

<style>
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

html {
  height: 100%;
}

body {
  height: 100%;
  background: url('/coffee_mug-matt-hoffman-unsplash.jpg') no-repeat center
    center fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  background-size: cover;
  -o-background-size: cover;
  font-size: 1.5em;
  font-family: 'Playfair Display', serif;
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

.nav-item > a {
  font-size: 1.25em;
  color: wheat !important;
}
.nav-item > a:hover {
  color: sienna !important;
}
</style>
