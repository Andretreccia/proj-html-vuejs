<template>
  <main id="site-main">
    <SectionComponent :ArrayX="SectionOne" />

    <SectionComponent :ArrayX="SectionTwo" />

    <SectionComponent :ArrayX="SectionGrid" />
  </main>
</template>

<script>
import SectionComponent from "./SectionComponent.vue";
export default {
  props: {
    SectionOne: Array,
    SectionTwo: Array,
    SectionGrid: Array,
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