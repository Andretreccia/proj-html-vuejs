<template>
  <main id="site-main">
    <SectionComponent :ArrayX="SectionOne" />

    <SectionComponent :ArrayX="SectionTwo" />

    <SectionComponent :ArrayX="SectionGrid" />

    <SectionComponent :ArrayX="SectionPlans" />

    <SectionComponent :ArrayX="SectionNews" />

    <SectionComponent :ArrayX="SectionClient" />
  </main>
</template>

<script>
import SectionComponent from "./SectionComponent.vue";
export default {
  props: {
    SectionOne: Array,
    SectionTwo: Array,
    SectionGrid: Array,
    SectionPlans: Array,
    SectionNews: Array,
    SectionClient: Array,
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