<template>
  <section class="">
    <div
      class="container-fluid text-center"
      v-bind:class="{
        bgblue: element.lay == 'blue',
      }"
      v-for="element in ArrayX[0]"
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
      <Cards3Component :ArrayX="ArrayX" v-if="element.if == '3card'" />
      <Cards4Component :ArrayX="ArrayX" v-if="element.if == '4card'" />
      <GridComponent :ArrayX="ArrayX" v-if="element.if == 'grid'" />
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
import Cards4Component from "./Cards4Component.vue";
import GridComponent from "./GridComponent.vue";
export default {
  props: {
    ArrayX: Array,
  },
  components: {
    Cards3Component,
    Cards4Component,
    GridComponent,
  },
};
</script>

<style lang="scss">
.bgblue {
  background-color: rgb(3, 3, 97);
}
</style>