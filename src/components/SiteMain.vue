<template>
  <main id="site-main">
    <div class="container-fluid text-center">
      <div class="text text-center">
        <h2 class="mb-4 fw-bold">
          Meet The New Agency SEO Template From The Avada Team
        </h2>
        <p>
          Sed ut perspiciatis unde omnis iste natus error sit voluptatem
          accusantium doloremque laudantium.
        </p>
      </div>
      <Cards3Component :ArrayOne="SectionOne" />
    </div>
    <img src="../assets/images/agency-seo-desk-front-1200x570.jpg" alt="" />
  </main>
</template>

<script>
import Cards3Component from "./Cards3Component.vue";
export default {
  props: {
    SectionOne: Array,
  },
  components: { Cards3Component },
};
</script>

<style lang="scss">
@import "../assets/scss/color.scss";
#site-main {
  background-color: $background-first;
}
</style>