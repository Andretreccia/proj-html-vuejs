<template>
  <div class="container">
    <div class="row d-flex justify-content-center p-5">
      <div class="col" v-for="element in ArrayX[1]" :key="element.qua">
        <div class="card text-center px-5 py-3 mt-2 mb-2">
          <!-- inizio degli elementi variabili -->

          <i :class="element.icon" class="mt-3 fs-3" v-if="element.icon"></i>
          <img
            class="img-fluid"
            :src="require('../assets/images/' + element.img)"
            alt=""
            v-if="element.img"
          />
          <h5 class="fw-bold fs-4 mt-4" v-if="element.title">
            {{ element.title }}
          </h5>
          <p class="mt-3 mb-5" v-if="element.text">
            {{ element.text }}
          </p>
          <a class="" href="" v-if="element.link">{{ element.link }}</a>

          <!-- se l'elemento è un prodotto -->

          <div v-if="element.product" class="mt-2 mb-2 product">
            <div
              style="height: 40px"
              class="d-flex justify-content-center mb-3"
            >
              <div>
                <i class="fas fa-dollar-sign"> </i>
              </div>
              <div class="fs-1 fw-bold price d-flex align-items-center">
                {{ element.price }}
              </div>
              <div
                class="
                  d-flex
                  flex-column
                  align-items-start
                  justify-content-between
                "
              >
                <span class="fw-bold price">99</span>
                <span class="monthly">monthly</span>
              </div>
            </div>
            <p>{{ element.feature1 }} Projects</p>
            <p>{{ element.feature2 }} Storage</p>
            <p>{{ element.feature3 }} Users</p>
            <button class="rounded-pill button_third" v-if="element.button">
              {{ element.button }}
            </button>
          </div>
          <div v-if="element.author">
            <span>{{ element.author }}, </span> <span>{{ element.role }}</span>
          </div>
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
a {
  text-decoration: none !important;
  color: $contrast-color !important;
}
</style>