<template>
  <header id="site-header">
    <Navbar :NavLinks="NavLinks" />
    <Jumbo />
  </header>
</template>

<script>
import Navbar from "./Navbar.vue";
import Jumbo from "./Jumbo.vue";
export default {
  props: {
    NavLinks: Array,
  },
  components: {
    Navbar,
    Jumbo,
  },
};
</script>

<style lang="scss">
#site-header {
  padding: 1rem;
  height: 800px;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  background-image: url(../assets/images/1-hero-image.png);
}
</style>