<template>
  <div id="app">
    <SiteHeader :NavLinks="NavLinks" />

    <SiteMain
      :SectionOne="SectionOne"
      :SectionTwo="SectionTwo"
      :SectionGrid="SectionGrid"
      :SectionPlans="SectionPlans"
      :SectionNews="SectionNews"
      :SectionClient="SectionClient"
      :SectionConsultant="SectionConsultant"
    />
    <SiteFooter :FooterSection="FooterSection" />
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
            theme: "section-one",
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
            theme: "section-two",
          },
        ],
        [
          {
            title: "Google SEO",
            text: "Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.",
            icon: "fab fa-google",
            link: "Read More ",
          },
          {
            title: "Brand Strategy",
            text: "Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.",
            icon: "fas fa-cog",
            link: "Read More ",
          },
          {
            title: "Local SEO",
            text: "Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.",
            icon: "fas fa-building",
            link: "Read More ",
          },
          {
            title: "SEO Analysis",
            text: "Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.",
            icon: "fas fa-chart-bar",
            link: "Read More ",
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
            theme: "section-grid",
          },
        ],
        [
          "case-study-gallery-3-1-400x300.jpg",
          "case-study-gallery-2-400x300.jpg",
          "case-study-gallery-1-1-400x300.jpg",
          "case-study-gallery-4-1-400x300.jpg",
          "case-study-gallery-5-1-400x300.jpg",
          "case-study-gallery-6-1-400x300.jpg",
        ],
      ],
      SectionPlans: [
        [
          {
            if: "plans",
            title: "Our Plans",
            text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.",
            theme: "section-plans",
          },
        ],
        [
          {
            title: "Standard",
            feature1: "5",
            feature2: "5 GB",
            feature3: "Unlimited",
            price: "19",
            button: "START TODAY",
            product: true,
          },
          {
            title: "Premium",
            feature1: "10",
            feature2: "15 GB",
            feature3: "Unlimited",
            price: "29",
            button: "START TODAY",
            product: true,
          },
          {
            title: "Professional",
            feature1: "15",
            feature2: "30 GB",
            feature3: "Unlimited",
            price: "39",
            button: "START TODAY",
            product: true,
          },
          {
            title: "Extreme",
            feature1: "Unlimited",
            feature2: "Unlimited",
            feature3: "Unlimited",
            price: "59",
            button: "START TODAY",
            product: true,
          },
        ],
      ],
      SectionNews: [
        [
          {
            if: "news",
            title: "Our News",
            text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.",
            theme: "section-news",
            button: "GO TO NEWS",
          },
        ],
        [
          {
            img: "related-service-2-320x202.jpg",
            title: "Whi You Need A SEO Agency Now",
            date: "November 1st, 2017",
            text: "ALorem ipsum dolor sit amet, consectetur adipiscing elit. In et scelerisque sem. Nunc molestie neque augue, at gravida mi blandit",
          },
          {
            img: "related-service-4-320x202.jpg",
            title: "SEO Tips For Your Startup",
            date: "November 1st, 2017",
            text: "ALorem ipsum dolor sit amet, consectetur adipiscing elit. In et scelerisque sem. Nunc molestie neque augue, at gravida mi blandit",
          },
          {
            img: "blog-post-6-320x202.jpg",
            title: "Image Optimization For Your Site",
            date: "November 1st, 2017",
            text: "ALorem ipsum dolor sit amet, consectetur adipiscing elit. In et scelerisque sem. Nunc molestie neque augue, at gravida mi blandit",
          },
        ],
      ],
      SectionClient: [
        [
          {
            if: "client",
            title: "What Our Client Say",
            theme: "section-client",
          },
        ],
        [
          {
            text: "Ability proceeds from a fusion of skills, knowledge, unferstanding and imagination, consolidated by experience.",
            author: "Luis Desalvo",
            img: "testimonials-2.jpg",
            role: "CREO TECH",
          },
        ],
        [
          "clients_partner_5-200x202.png",
          "clients_partner_6-200x202.png",
          "clients_partner_1-200x202.png",
          "clients_partner_2-200x202.png",
        ],
      ],
      SectionConsultant: [
        [
          {
            if: "consultant",
            theme: "section-consultant",
            title: "Start Your Free Consultation",
            text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.",
            button: "CONTACT US NOW",
          },
        ],
      ],
      /*
       footer
        */

      FooterSection: [
        [
          {
            theme: "footer",
            img: "logo_seo_1x.png",
            copyright: "2012-2020",
            themeBy: "ThemeFusion",
            poweredBy: "WordPress",
            facebook: "fab fa-facebook-f",
            instagram: "fab fa-instagram",
            twitter: "fab fa-instagram",
            youtube: "fab fa-youtube",
          },
        ],
        [
          "Home",
          "Who We Are",
          "What We Do",
          "Where We Work",
          "Careers",
          "News",
          "Get in Touch Now",
        ],
        [
          "fab fa-facebook-f",
          "fab fa-instagram",
          "fab fa-twitter",
          "fab fa-youtube",
        ],
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../node_modules/bootstrap/scss/bootstrap.scss";
@import "./assets/scss/color.scss";
@import url("https://fonts.googleapis.com/css2?family=Source+Sans+Pro:ital,wght@0,200;0,300;0,400;0,600;0,700;0,900;1,200;1,300;1,400;1,600;1,700;1,900&display=swap");
#app {
  font-family: "Source Sans Pro", sans-serif;

  button {
    font-size: 15px;
    color: white;
    margin-right: 1rem;
    margin-bottom: 3rem;
    border-style: none;
    padding: 0.7rem 2rem;
    background: none;
    font-weight: 500;
    &:hover {
      transition: 0.5s;
      filter: brightness(1.1);
    }
  }
  .button_first {
    background-color: $contrast-color;
  }
  .button_second {
    background-color: $contrast-color-secondary;
  }
  .button_third {
    border: 2px solid black;
    color: black;
    margin-left: 4rem;
    margin-right: 4rem;
    margin-bottom: 0;
    &:hover {
      border: 2px solid $contrast-color;
      transition: 0.5s;
      color: white;
      background: $contrast-color;
    }
  }
  a {
    color: white;
    text-decoration: none;
    &:hover {
      transition: 0.5s;
      color: $contrast-color;
    }
  }
}
</style>
