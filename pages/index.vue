<template>
  <div>
    <b-nav>
      <b-nav-item active>3rdwave</b-nav-item>
      <b-nav-item>pricing</b-nav-item>
      <b-nav-item>what we do</b-nav-item>
    </b-nav>
    <div id="pond">
      <h1 class="heading">
        your orders.
        <br />
        <span class="italic">
          ready for pick up.
        </span>
      </h1>
    </div>
  </div>
</template>

<script>
export default {
  components: {}
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;1,700&display=swap');

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

#pond {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 94vh;
}

.heading {
  position: relative;
  color: wheat;
}

.italic {
  font-style: italic;
}
</style>
