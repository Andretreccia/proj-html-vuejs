<template>
  <nav class="navbar">
    <div class="container d-flex justify-content-between">
      <!-- nav logo -->
      <div class="logo text-light">
        <img src="../assets/images/logo_seo_w_1x.png" alt="" />
      </div>
      <!-- links nav -->
      <div class="links d-flex justify-content-between align-items-center">
        <a
          href=""
          class="nav-links"
          v-for="NavLink in NavLinks"
          :key="NavLink.i"
          >{{ NavLink.link }}
          <span class="apply" v-if="NavLink.apply == true">APPLY</span></a
        >
      </div>
      <div class="d-flex align-items-center">
        <button class="button_first px-4 py-2 rounded-pill text-white fw-bold">
          GET IN TOUCH NOW
        </button>
      </div>
      <!-- nav btn -->
    </div>
  </nav>
</template>

<script>
export default {
  props: {
    NavLinks: Array,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/color.scss";
.navbar {
  .logo {
    cursor: pointer;
  }
  .nav-links {
    display: block;
    padding: 0.5rem 1rem;
    text-decoration: none;
    transition: color 0.15s ease-in-out, background-color 0.15s ease-in-out,
      border-color 0.15s ease-in-out;
    .apply {
      font-size: 0.8rem;
      border-radius: 5px;
      padding: 0.2rem 0.5rem;
      border: 1px solid $contrast-color;
      color: $contrast-color;
    }
  }
  button {
    margin: 0 !important;
  }
}
</style>