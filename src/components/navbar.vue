<template>
  <nav class="navbar">
    <div class="container d-flex justify-content-between">
      <!-- nav logo -->
      <div class="logo text-light">
        <img src="../assets/images/logo_seo_w_1x.png" alt="" />
      </div>
      <!-- links nav -->
      <div class="links d-flex justify-content-between">
        <a href="" class="nav-link" v-for="NavLink in NavLinks" :key="NavLink.i"
          >{{ NavLink.link }}
          <span class="apply" v-if="NavLink.apply == true">APPLY</span></a
        >
        <button class="nav_button px-4 py-2 rounded-pill text-white fw-bold">
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
  .links {
    a {
      color: white;
      &:hover {
        transition: 0.5s;
        color: $contrast-color;
      }
    }
    .apply {
      font-size: 0.8rem;
      border-radius: 5px;
      padding: 0.2rem 0.5rem;
      border: 1px solid $contrast-color;
      color: $contrast-color;
    }
  }
  .nav_button {
    border-style: none;
    background-color: $contrast-color;
    &:hover {
      transition: 0.5s;
      filter: brightness(1.1);
    }
  }
}
</style>