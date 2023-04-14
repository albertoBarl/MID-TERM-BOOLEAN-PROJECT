<template lang="">
  <!-- newsletter -->
  <div class="newsletter">
    <newsletter />
  </div>

  <!-- proper footer -->
  <div class="container mt-5">
    <!-- row 1 -->
    <div class="row d-flex" v-for="(item, index) in idata">
      <!-- address section -->
      <section class="address col-4">
        <h5>Address</h5>
        <p v-for="(item, index) in idata[index].addressSect">
          {{ item }}
        </p>
        <socials />
      </section>

      <!-- explore section -->
      <section class="col-2">
        <h5>Explore</h5>
        <ul
          v-for="(item, index) in idata[index].exploreSect"
          class="list-unstyled"
        >
          <li>
            <a href="/">{{ item }}</a>
          </li>
        </ul>
      </section>

      <!-- information section -->
      <section class="col-2">
        <h5>Information</h5>
        <ul
          v-for="(item, index) in idata[index].informationSect"
          class="list-unstyled"
        >
          <li>
            <a href="/">{{ item }}</a>
          </li>
        </ul>
      </section>

      <!-- instagram section -->
      <section class="col-4">
        <div class="d-flex align-items-center gap-2">
          <h5 class="">Instagram</h5>
          <a href="/"><span class="instaTag">@maxcoach</span></a>
        </div>
        <div class="d-flex gap-5">
          <div
            class="sPost"
            v-for="(item, index) in idata[index].instaPosts"
            :class="[index] > 2 ? 'd-none' : ''"
          >
            <img :src="`src/assets/images/${item}`" alt="not available" />
          </div>
        </div>
      </section>
    </div>

    <!-- row 2 -->
    <div class="row rights">
      <div class="col-12 d-flex justify-content-center">
        &copy; 2020 Maxcoach. All Rights Reserved
      </div>
    </div>
  </div>
</template>

<!-- script -->
<script>
import socials from "./elements/socials.vue";
import newsletter from "./elements/newsletter.vue";

export default {
  components: {
    socials,
    newsletter,
  },
  props: {
    idata: Array,
  },
};
</script>

<!-- style -->
<style lang="scss" scoped>
@use "../styles/generals.scss" as *;
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.newsletter {
  background-color: #2b4081;
  padding: 75px;
}

* {
  line-height: 2.5;
}
.rights {
  padding-top: 100px;
}

.sPost {
  width: 150px;
  img {
    width: 100%;
  }
}

a,
p {
  color: grey;
  text-decoration: none;
}
a:hover {
  color: $aranciata;
}

.address {
  p:nth-child(4):hover {
    color: $aranciata;
    cursor: pointer;
  }
}

.instaTag {
  color: $aranciata;
}

.col-12 {
  color: rgb(193, 191, 191);
}
</style>
