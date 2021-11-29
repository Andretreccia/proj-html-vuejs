<template>
  <footer id="site-footer">
    <div
      class="container d-flex flex-column align-items-center"
      v-for="element in FooterSection[0]"
      :key="element.u"
    >
      <img
        :src="require('../assets/images/' + element.img)"
        alt=""
        v-if="element.img"
      />
      <div class="py-5">
        <a
          class="footer-links"
          href=""
          v-for="element in FooterSection[1]"
          :key="element.el"
        >
          {{ element }}</a
        >
      </div>
      <div class="reference">
        <p>
          &#9400;Copyright 2012-2020 | Avada Theme by
          <span>{{ element.themeBy }}</span> | All Rights Reserved | Powered by
          <span>{{ element.poweredBy }}</span>
        </p>
        <div class="text-center py-3">
          <i
            v-for="element in FooterSection[2]"
            :key="element.icon"
            :class="element"
            class="m-2 fs-4"
          >
          </i>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  props: {
    FooterSection: Array,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/color.scss";
#site-footer {
  background: $background-first;
  padding: 3rem 0rem;
  color: $text-general;
  .footer-links {
    color: black;
    margin: 4rem 1rem;
  }
  .reference span {
    color: black;
    font-weight: 600;
  }
  i {
    cursor: pointer;
  }
}
</style>