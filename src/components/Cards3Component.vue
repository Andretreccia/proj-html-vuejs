<template>
  <div class="container pt-5">
    <div class="row d-flex justify-content-center">
      <div class="col-4" v-for="element in ArrayX[1]" :key="element.qua">
        <div class="card text-center px-5 py-5">
          <img
            :src="require('../assets/images/' + element.img)"
            alt=""
            v-if="element.img"
          />
          <i :class="element.icon" class="mt-3 fs-3" v-if="element.icon"></i>
          <h5 class="fw-bold fs-4 mt-4" v-if="element.title">
            {{ element.title }}
          </h5>
          <span v-if="element.date">{{ element.date }}</span>
          <p class="mt-3 mb-5" v-if="element.text">
            {{ element.text }}
          </p>
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
.text {
  width: 500px;
  margin: auto;
  margin-bottom: 4rem;
}
.row {
  .card {
    border: none;
    i {
      color: $contrast-color;
    }
  }
}
</style>