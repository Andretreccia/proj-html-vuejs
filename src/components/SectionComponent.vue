<template>
  <section class="pt-5">
    <div
      class="container-fluid text-center"
      v-for="element in ArrayOne[0]"
      :key="element.op"
    >
      <div class="text text-center">
        <h2 class="pt-4 mb-4 fw-bold" v-if="element.title">
          {{ element.title }}
        </h2>
        <p v-if="element.text">
          {{ element.text }}
        </p>
      </div>
      <Cards3Component :ArrayOne="ArrayOne" />
      <img
        :src="require('../assets/images/' + element.img)"
        alt=""
        v-if="element.img"
      />
    </div>
  </section>
</template>

<script>
import Cards3Component from "./Cards3Component.vue";
export default {
  props: {
    ArrayOne: Array,
  },
  components: {
    Cards3Component,
  },
};
</script>

<style lang="scss">
</style>