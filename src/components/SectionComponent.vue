<template>
  <section class="">
    <div
      class="container-fluid text-center"
      v-bind:class="{
        sectionOne: element.theme == 'section-one',
        sectionTwo: element.theme == 'section-two',
        sectionPlans: element.theme == 'section-plans',
        sectionNews: element.theme == 'section-news',
        sectionClient: element.theme == 'section-client',
        sectionGrid: element.theme == 'section-grid',
        sectionConsultant: element.theme == 'section-consultant',
      }"
      v-for="element in ArrayX[0]"
      :key="element.sec"
    >
      <div class="container-fluid py-5">
        <div class="text text-center">
          <h2 class="pt-4 mb-4 fw-bold" v-if="element.title">
            {{ element.title }}
          </h2>
          <p class="fs-5" v-if="element.text">
            {{ element.text }}
          </p>
        </div>
        <CardsComponent :ArrayX="ArrayX" v-if="element.if == '3card'" />
        <CardsComponent :ArrayX="ArrayX" v-if="element.if == '4card'" />
        <GridComponent :ArrayX="ArrayX" v-if="element.if == 'grid'" />
        <CardsComponent :ArrayX="ArrayX" v-if="element.if == 'plans'" />
        <CardsComponent :ArrayX="ArrayX" v-if="element.if == 'news'" />
        <CardsComponent :ArrayX="ArrayX" v-if="element.if == 'client'" />
        <hr class="m-auto" :ArrayX="ArrayX" v-if="element.if == 'client'" />
        <GridComponent :ArrayX="ArrayX" v-if="element.if == 'client'" />
        <button class="rounded-pill button_first" v-if="element.button">
          {{ element.button }}
        </button>
      </div>
      <img
        :src="require('../assets/images/' + element.img)"
        alt=""
        v-if="element.img"
      />
    </div>
  </section>
</template>

<script>
import CardsComponent from "./CardsComponent.vue";
import GridComponent from "./GridComponent.vue";
export default {
  props: {
    ArrayX: Array,
  },
  components: {
    CardsComponent,
    GridComponent,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/color.scss";

/* Prima sezione */
.sectionOne {
  .card {
    transition: 0.3s;
    padding: 0 2rem;
    bottom: 0;
    &:hover {
      bottom: 10px;
      h5 {
        color: $contrast-color;
        transition: 0.3s;
      }
    }
  }
}
.sectionTwo {
  background-color: $background-section-two;
  background-image: url(../assets/images/pattern_background.png);
  background-position: center;
  color: white;
  height: 1000px;
  .card {
    bottom: 0;
    background-color: $background-section-two-element;
    padding: 0 3rem;
    height: 400px;
    transition: 0.3s;
    &:hover {
      bottom: 10px;
    }
    a {
      color: $contrast-color !important;
      font-size: 1.2rem;
    }
  }
}
.sectionGrid {
  .row {
    flex-wrap: wrap;
    justify-content: center;
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
      .price {
        font-weight: 600;
      }

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
        font-weight: 900;
      }
    }
  }
}
.sectionNews {
  .card {
    background: none;
    h5 {
      color: $contrast-color;
    }
    span {
      font-size: 14px;
    }
    p {
      font-size: 17px;
    }
    img {
      transition: 0.5s;
      transform: scale(1);
      &:hover {
        transition: 0.5s;
        transform: scale(1.1);
        border-radius: 5px;
      }
    }
  }
}
.sectionClient {
  background: white;
  .card {
    width: 800px;
    margin: auto;
    img {
      width: 150px;
      border-radius: 100%;
      margin: auto;
    }
    p {
      font-style: italic;
      font-size: 21px;
    }
    .author {
      font-weight: bold;
    }
  }
  .grid {
    padding: 0;
    .row {
      margin: -1rem;
      padding-top: 3rem;
      .col {
        width: 150px;
        img {
          height: 120px;
          cursor: pointer;
          transform: scale(1);
          transition: 0.5s;
          &:hover {
            transition: 0.5s;
            transform: scale(1.2);
          }
        }
      }
    }
  }
}
.sectionConsultant {
  background: url(../assets/images/CTA-seo-1.jpg);
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  padding: 0 !important;
  .container-fluid {
    backdrop-filter: brightness(0.5);

    .text {
      color: white;
      position: relative;
    }
  }
}
hr {
  width: 90%;
  margin: auto;
}
</style>