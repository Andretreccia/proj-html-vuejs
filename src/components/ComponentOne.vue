<template>
  <div class="container-fluid text-center">
    <div class="container pt-5">
      <div class="text text-center">
        <h2 class="mb-4 fw-bold">
          Meet The New Agency SEO Template From The Avada Team
        </h2>
        <p>
          Sed ut perspiciatis unde omnis iste natus error sit voluptatem
          accusantium doloremque laudantium.
        </p>
      </div>
      <div class="row d-flex justify-content-center">
        <div
          class="col-4"
          v-for="SectionOnecard in SectionOne"
          :key="SectionOnecard"
        >
          <div class="card text-center px-5 py-5">
            <i :class="SectionOnecard.icon" class="mt-3 fs-3"></i>
            <h5 class="fw-bold fs-4 mt-4">{{ SectionOnecard.title }}</h5>
            <p class="mt-3 mb-5">{{ SectionOnecard.text }}</p>
          </div>
        </div>
      </div>
    </div>
    <img src="../assets/images/agency-seo-desk-front-1200x570.jpg" alt="" />
  </div>
</template>


<script>
export default {
  props: {
    SectionOne: Array,
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