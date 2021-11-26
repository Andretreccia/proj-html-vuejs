<template>
  <div class="container pt-5">
    <div class="row d-flex justify-content-center p-5">
      <div class="col-3" v-for="element in ArrayX[1]" :key="element.qua">
        <div class="card text-center px-5 py-5">
          <i :class="element.icon" class="mt-3 fs-3" v-if="element.icon"></i>
          <h5 class="fw-bold fs-4 mt-4" v-if="element.title">
            {{ element.title }}
          </h5>
          <p class="mt-3 mb-5" v-if="element.text">
            {{ element.text }}
          </p>
          <a class="" href="" v-if="element.link">{{ element.link }}</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    ArrayX: Array,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/color.scss";

a {
  text-decoration: none !important;
  color: $contrast-color !important;
}
</style>