<template>
  <section class="pt-4">
    <div
      class="container-fluid text-center py-5"
      v-bind:class="{
        sectionTwo: element.theme == 'section-two',
        sectionPlans: element.theme == 'section-plans',
        sectionNews: element.theme == 'section-news',
        sectionClient: element.theme == 'section-client',
        sectionGrid: element.theme == 'section-grid',
      }"
      v-for="element in ArrayX[0]"
      :key="element.op"
    >
      <div class="text text-center">
        <h2 class="pt-5 mb-4 fw-bold" v-if="element.title">
          {{ element.title }}
        </h2>
        <p v-if="element.text">
          {{ element.text }}
        </p>
      </div>
      <Cards4Component :ArrayX="ArrayX" v-if="element.if == '3card'" />
      <Cards4Component :ArrayX="ArrayX" v-if="element.if == '4card'" />
      <GridComponent :ArrayX="ArrayX" v-if="element.if == 'grid'" />
      <Cards4Component :ArrayX="ArrayX" v-if="element.if == 'plans'" />
      <Cards4Component :ArrayX="ArrayX" v-if="element.if == 'news'" />
      <Cards4Component :ArrayX="ArrayX" v-if="element.if == 'client'" />
      <hr :ArrayX="ArrayX" v-if="element.if == 'client'" />
      <GridComponent :ArrayX="ArrayX" v-if="element.if == 'client'" />

      <img
        :src="require('../assets/images/' + element.img)"
        alt=""
        v-if="element.img"
      />
      <button class="rounded-pill button_first" v-if="element.button">
        {{ element.button }}
      </button>
    </div>
  </section>
</template>

<script>
//import Cards3Component from "./Cards3Component.vue";
import Cards4Component from "./Cards4Component.vue";
import GridComponent from "./GridComponent.vue";
export default {
  props: {
    ArrayX: Array,
  },
  components: {
    //Cards3Component,
    Cards4Component,
    GridComponent,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/color.scss";

/* Prima sezione */

.sectionTwo {
  background-color: $background-section-two;
  background-image: url(../assets/images/pattern_background.png);
  background-position: center;
  color: white;
  height: 1000px;
  .card {
    background-color: $background-section-two-element;
  }
}
.sectionGrid {
  .row {
    flex-wrap: wrap;
    justify-content: center;
    .col {
      width: 500px;
    }
  }
}
.sectionPlans {
  background: url(../assets/images/background1.jpg);
  background-size: cover;
  color: white;
  .card {
    color: $text-general;

    .product {
      height: 300px;
      display: flex;
      flex-direction: column;
      justify-content: space-around;

      i {
        color: $text-general;
      }
      .monthly {
        font-style: italic;
        font-size: 12px;
        font-weight: bold;
      }
      .price {
        color: $contrast-color-secondary;
      }
    }
  }
}
.sectionNews {
  .card {
    background: none;
  }
}
.sectionClient {
  background: white;
  .card {
    img {
      width: 250px;
      border-radius: 100%;
      margin: auto;
    }
    p {
      font-style: italic;
      font-size: 24px;
    }
  }
}
</style>