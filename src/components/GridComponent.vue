<template>
  <div class="container">
    <div class="row">
      <div class="col-4 p-2" v-for="element in ArrayX[1]" :key="element">
        <img
          class="w-100"
          :src="require('../assets/images/' + element)"
          alt=""
        />
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