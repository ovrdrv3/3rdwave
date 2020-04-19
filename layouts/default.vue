<template>
  <div>
    <b-navbar toggleable="lg">
      <b-navbar-brand to="/" exact>3rdwave</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item to="/what-we-do" exact>what we do</b-nav-item>
          <b-nav-item>pricing</b-nav-item>
          <b-nav-item>contact us</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
    <nuxt />
  </div>
</template>

<script>
export default {
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
<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;1,700&display=swap');
$bg: wheat;
$font-color: sienna;
$contrast-color: slategray;
$contrast-color-2: khaki;
$break-small: 600px;
$break-large: 1000px;
html {
  height: 100%;
}

body {
  height: 100%;
  font-size: 1.5em;
  font-family: 'Playfair Display', serif;
  color: $font-color;
  background-color: Beige;
}

.btn-primary:hover,
.btn-primary:focus,
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: $font-color !important;
  border-color: $contrast-color-2 !important;
  background-color: $contrast-color-2 !important;
}

.btn-primary {
  color: $bg !important;
  background-color: $font-color !important;
  border-color: $font-color !important;
}

.stand-out-font {
  color: $bg;
}

.bg-font-color-text {
  color: $font-color;
}

.primary-font-color-bg {
  background-color: $bg;
}

.italic {
  font-style: italic;
}

.order-card {
  font-size: 0.75em;
  font-family: 'Lucida Console', Monaco, monospace;
  background-color: $contrast-color;
}
.nav-link,
.navbar-brand {
  font-size: 1.25em;
  color: $bg !important;
}
.nav-link:hover,
.navbar-brand:hover,
.nuxt-link-active {
  color: $font-color !important;
}
</style>
