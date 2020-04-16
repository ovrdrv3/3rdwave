<template>
  <b-container>
    <b-row class="py-5">
      <b-col>
        <b-card
          class="bg-font-color-text rounded mx-auto primary-font-color-bg"
        >
          <h2>
            your orders.
            <br />
            <span class="italic">
              ready for pick up.
            </span>
          </h2>
          <b-button variant="primary" class="font color-bg "
            >Contact Us</b-button
          >
        </b-card>
      </b-col>
      <b-col
        ><b-card class="notification-text order-card" no-body>
          <b-list-group>
            <b-list-group-item>
              <b-card-title>Donaven</b-card-title>
              <b-card-sub-title class="mb-4">dine-in</b-card-sub-title>
              <b-card-text>
                Medium Americano
              </b-card-text>
              <b-card-sub-title class="mb-4">Room for cream</b-card-sub-title>
              <b-card-text>
                Pourover
              </b-card-text>
              <b-card-sub-title class="mb-4">Ethiopian</b-card-sub-title>
              <b-card-text>
                Vegan Maple donut
              </b-card-text>
              <b-button href="#" variant="primary">Ready</b-button>
            </b-list-group-item>

            <b-list-group-item>
              <b-card-title>Rocio</b-card-title>
              <b-card-sub-title class="mb-2">to-go</b-card-sub-title>
              <b-card-text>
                Medium Vanilla Latte
              </b-card-text>
              <b-button href="#" variant="primary">Ready</b-button>
            </b-list-group-item>
          </b-list-group>
        </b-card></b-col
      >
    </b-row>
  </b-container>
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

<style lang="scss">
$bg: wheat;
$font-color: sienna;
$break-small: 600px;
$break-large: 1000px;
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;1,700&display=swap');
.btn-primary:hover,
.btn-primary:focus,
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: $bg !important;
  background-color: $font-color !important;
  border-color: $font-color !important;
}

.btn-primary {
  border-color: $bg !important;
}

.bg-font-color-text {
  color: $font-color;
}

.color-bg {
  background-color: $font-color;
}

.font {
  color: $bg;
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
}
</style>
