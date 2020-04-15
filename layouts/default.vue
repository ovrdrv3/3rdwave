<template>
  <div>
    <b-navbar toggleable="lg" variant="light">
      <b-navbar-brand class="" href="/">3rdwave</b-navbar-brand>

      <b-navbar-toggle variant="light" target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item>what we do</b-nav-item>
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
<style>
html {
  height: 100%;
}

body {
  height: 100%;
  font-size: 1.5em;
  font-family: 'Playfair Display', serif;
}
.nav-link,
.navbar-brand {
  font-size: 1.25em;
  color: wheat !important;
}
.nav-link:hover,
.navbar-brand:hover {
  color: sienna !important;
}
</style>
