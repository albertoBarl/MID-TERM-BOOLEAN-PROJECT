<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Main from "./components/Main.vue";
import eventscount from "./components/elements/eventscount.vue";

export default {
  components: {
    // main components
    Header,
    Footer,
    Main,
    // others
    eventscount,
  },
  data() {
    return {
      navbar: [
        {
          section: "Home",
          dropdowns: [
            "MaxCoach Education",
            "Course Portal",
            "Distance Learning",
            "Multimedia Pedagogy",
            "Modern Scrolling",
            "Remote Training",
            "Healt Coaching",
            "Gym Coaching",
            "Business",
            "Artist",
            "Kitchen Coach",
            "Motivation",
            "Dancing",
            "Guitar",
            "Yoga",
            "Photography",
            "Personal Finance",
            "Sales Coaching",
            "Mental Therapy",
          ],
        },
        {
          section: "Pages",
          dropdowns: [
            "Start Here",
            "Succes Story",
            "About me",
            "About us 01",
            "About us 02",
            "About us 03",
            "Contact me",
            "Contact us",
            "Purchase Guide",
            "Privacy Policy",
            "Terms of Service",
          ],
        },
        {
          section: "Courses",
          dropdowns: [
            "Course Gride 01",
            "Course Gride 02",
            "Course Gride 03",
            "Membership Levels",
            "Become a Teacher",
            "Profile",
            "Checkout",
            "Single Layout",
          ],
        },
        { section: "Features", dropdowns: ["Events", "Zoom Meetings"] },
        {
          section: "Blog",
          dropdowns: ["Blog Grid", "Blog Masonry", "Blog Classic", "Blog List"],
        },
        {
          section: "Shop",
          dropdowns: [
            "Shop Left Sidebar",
            "Shop Right Sidebar",
            "Cart",
            "Wishlist",
            "Single Product",
          ],
        },
      ],
      footerData: [
        {
          addressSect: [
            "382 NE 191st St # 87394 Miami, FL 33179-3899",
            "+1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)",
            "support@maxcoach.com",
          ],

          exploreSect: [
            "Start here",
            "Success story",
            "Blog",
            "Courses",
            "Contact us",
          ],

          informationSect: [
            "Membership",
            "Purchase Guide",
            "Privacy policy",
            "Terms of services",
          ],

          instaPosts: [
            "120084500_197897808368764_8114555493043279565_n.jpg",
            "120012142_177596140500760_8623485824101406058_n.jpg",
            "120099363_364334431619755_7198812647386067017_n.jpg",
            "artist-event-01-250x300.jpg",
            "artist-hero-image-02.jpg",
            "artist-course-06-480x480.jpg",
            "artist-hero-image-01.jpg",
            "artist-hero-image-03.png",
            "artist-hero-image-04.jpg",
          ],
        },
      ],
    };
  },
};
</script>

<template>
  <div class="eventscount">
    <eventscount />
  </div>
  <div class="header">
    <Header :navbar="navbar" :key="index" />
  </div>
  <div class="main">
    <Main />
  </div>
  <div class="footer">
    <Footer :idata="footerData" :key="index" />
  </div>
</template>

<style lang="scss" scoped>
@use "./styles/generals.scss" as *;
@use "./styles/partials/mixins" as *;
@use "./styles/partials/variables" as *;

.eventscount {
  background-color: $d-wall;
  z-index: 5;
}

.header {
  background-color: $wall;
}

.footer {
  background-color: $d-wall;
}
</style>
