<template>
  <div class="container pt-5">
    <div class="row d-flex justify-content-center">
      <div class="col-3" v-for="element in ArrayOne" :key="element.qua">
        <div class="card text-center px-5 py-5">
          <i :class="element.icon" class="mt-3 fs-3" v-if="element.icon"></i>
          <h5 class="fw-bold fs-4 mt-4" v-if="element.title">
            {{ element.title }}
          </h5>
          <p class="mt-3 mb-5" v-if="element.text">
            {{ element.text }}
          </p>
          <a href="" v-if="element.link">{{ element.link }}</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    ArrayOne: Array,
  },
};
</script>

<style lang="scss">
</style>