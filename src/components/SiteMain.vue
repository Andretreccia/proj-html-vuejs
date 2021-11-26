<template>
  <main id="site-main">
    <SectionComponent :ArrayOne="SectionOne" />
  </main>
</template>

<script>
/* import Cards3Component from "./Cards3Component.vue";
import Cards4Component from "./Cards4Component.vue"; */
import SectionComponent from "./SectionComponent.vue";
export default {
  props: {
    SectionOne: Array,
    SectionTwo: Array,
  },
  components: { SectionComponent },
};
</script>

<style lang="scss">
@import "../assets/scss/color.scss";
#site-main {
  background-color: $background-first;
}
</style>