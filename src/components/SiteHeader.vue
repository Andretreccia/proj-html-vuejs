<template>
  <header id="site-header">
    <Navbar />

    <Jumbo />
  </header>
</template>

<script>
import Navbar from "./Navbar.vue";
import Jumbo from "./Jumbo.vue";
export default {
  components: {
    Navbar,
    Jumbo,
  },
};
</script>

<style lang="scss">
#site-header {
  height: 600px;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: right;
  background-image: url(../assets/images/1-hero-image.png);
}
</style>