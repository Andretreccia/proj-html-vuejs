<template>
  <div id="app">
    <SiteHeader :NavLinks="NavLinks" />

    <SiteMain :SectionOne="SectionOne" :SectionTwo="SectionTwo" />

    <SiteFooter />
  </div>
</template>

<script>
import SiteHeader from "./components/SiteHeader.vue";
import SiteMain from "./components/SiteMain.vue";
import SiteFooter from "./components/SiteFooter.vue";

export default {
  name: "App",
  components: {
    SiteHeader,
    SiteMain,
    SiteFooter,
  },
  data() {
    return {
      /*
         header
         */
      NavLinks: [
        {
          link: "Home",
          apply: false,
        },
        {
          link: "Who We Are",
          apply: false,
        },
        {
          link: "What We Do",
          apply: false,
        },
        {
          link: "Where We Work",
          apply: false,
        },
        {
          link: "Careers",
          apply: true,
        },
        {
          link: "News",
          apply: false,
        },
      ],
      /*
         main 
         */
      SectionOne: [
        [
          {
            if: "3card",
            title: "Meet The New Agency SEO Template From The Avada Team",
            text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.",
            img: "agency-seo-desk-front-1200x570.jpg",
          },
        ],
        [
          {
            title: "Establish Goals",
            text: "Aliquam non elit lacus. Praesent aliquet, ipsum id scelerisque convallis, mi ligula euismod odio, vel dictum mi risus a mi.",
            icon: "fas fa-road",
          },
          {
            title: "Work With a Team",
            text: "Cras semper auctor aliquam. Sed porta sed lacus sit amet consectetur. Lorem ipsum dolor sit amet, consectetur adipiscin.",
            icon: "fas fa-video",
          },
          {
            title: "Get Results",
            text: "Vestibulum scelerisque egestas lectus sit amet molestie. Donec consectetur cursus est sed blandit. Nunc sed risus lacus.",
            icon: "fas fa-tint",
          },
        ],
      ],
      SectionTwo: [
        [
          {
            if: "4card",
            title: "See Our Top Notch Services",
            text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.",
            background: "pattern_background.png",
          },
        ],
        [
          {
            title: "Google SEO",
            text: "Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.",
            icon: "fab fa-google",
            link: "Read More >",
          },
          {
            title: "Brand Strategy",
            text: "Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.",
            icon: "fas fa-cog",
            link: "Read More >",
          },
          {
            title: "Local SEO",
            text: "Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.",
            icon: "fas fa-building",
            link: "Read More >",
          },
          {
            title: "SEO Analysis",
            text: "Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.",
            icon: "fas fa-chart-bar",
            link: "Read More >",
          },
        ],
      ],
      SectionGrid: [
        [
          {
            if: "grid",
            title: "Our Work",
            text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.",
            button: "VIEW OUR WORK",
          },
        ],
        [
          "case-study-gallery-1-1-600x450.jpg",
          "case-study-gallery-2-1-600x450.jpg",
          "case-study-gallery-3-1-600x450.jpg",
          "case-study-gallery-4-1-600x450.jpg",
          "case-study-gallery-5-1-600x450.jpg",
          "case-study-gallery-6-1-600x450.jpg",
        ],
      ],
      SectionPlans: [
        {
          title: "Standard",
          projects: "5 GB",
          storage: "",
          users: "",
          price: "19",
        },
        {
          title: "Premium",
          projects: "10 GB",
          storage: "",
          users: "",
          price: "29",
        },
        {
          title: "Professional",
          projects: "15 GB",
          storage: "",
          users: "",
          price: "39",
        },
        {
          title: "Extreme",
          projects: "Unlimited",
          storage: "Unlimited",
          users: "Unlimited",
          price: "59",
        },
      ],
      SectionNews: [
        {
          title: "Whi You Need A SEO Agency Now",
          date: "November 1st, 2017",
          text: "ALorem ipsum dolor sit amet, consectetur adipiscing elit. In et scelerisque sem. Nunc molestie neque augue, at gravida mi blandit",
        },
        {
          title: "SEO Tips For Your Startup",
          date: "November 1st, 2017",
          text: "ALorem ipsum dolor sit amet, consectetur adipiscing elit. In et scelerisque sem. Nunc molestie neque augue, at gravida mi blandit",
        },
        {
          title: "Image Optimization For Your Site",
          date: "November 1st, 2017",
          text: "ALorem ipsum dolor sit amet, consectetur adipiscing elit. In et scelerisque sem. Nunc molestie neque augue, at gravida mi blandit",
        },
      ],
      /*
       footer
        */

      footerLink: [
        "Home",
        "Who We Are",
        "Where We Work",
        "Careers",
        "News",
        "Get In Touch Now",
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../node_modules/bootstrap/scss/bootstrap.scss";
</style>
