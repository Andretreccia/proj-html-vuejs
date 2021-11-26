<template>
  <main id="site-main">
    <ComponentOne :SectionOne="SectionOne" />
  </main>
</template>

<script>
import ComponentOne from "./ComponentOne.vue";
export default {
  props: {
    SectionOne: Array,
  },
  components: { ComponentOne },
};
</script>

<style lang="scss">
@import "../assets/scss/color.scss";
#site-main {
  background-color: $background-first;
}
</style>