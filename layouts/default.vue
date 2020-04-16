<template>
  <div>
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
$primary-font-color: wheat;
$bg-font-color: sienna;
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}
.nav-link,
.navbar-brand {
  font-size: 1.25em;
  color: $primary-font-color !important;
}
.nav-link:hover,
.navbar-brand:hover {
  color: $bg-font-color !important;
}
</style>
