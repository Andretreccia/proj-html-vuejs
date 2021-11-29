<template>
  <div class="container py-4 mb-3 grid">
    <div class="row">
      <div
        class="col py-3"
        v-for="element in ArrayX[ArrayX.length - 1]"
        :key="element"
      >
        <img :src="require('../assets/images/' + element)" alt="" />
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
</style>