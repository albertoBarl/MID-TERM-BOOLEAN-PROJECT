<template lang="">
  <!-- proper header -->
  <div class="container" style="height: 75px">
    <div class="row d-flex align-items-center">
      <!-- logo -->
      <div class="col-4">
        <div class="pLogo">
          <a href="/"
            ><img src="src/assets/images/dark-logo.png" alt="logo"
          /></a>
        </div>
      </div>

      <!-- nav -->
      <div class="col-4 d-flex justify-content-center">
        <div class="d-flex gap-5">
          <div class="dropdown" v-for="(item, index) in navbar" :key="index">
            <label
              class="d-flex"
              data-bs-toggle="dropdown"
              aria-expanded="false"
            >
              {{ navbar[index].section }}
            </label>
            <ul class="dropdown-menu rounded-0 border-0 mt-3 list-unstyled">
              <li
                class="dropdown-item"
                v-for="(item, index) in navbar[index].dropdowns"
                :key="index"
              >
                {{ item }}
              </li>
            </ul>
          </div>
        </div>
      </div>

      <!-- socials -->
      <div class="col-4 d-flex justify-content-end">
        <socials />
      </div>
    </div>
  </div>
</template>

<!-- script -->
<script>
import socials from "./elements/socials.vue";

export default {
  components: {
    socials,
  },
  props: {
    navbar: Array,
  },
};
</script>

<!-- style -->
<style lang="scss" scoped>
@use "../styles/generals.scss" as *;
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.pLogo {
  width: 150px;
  img {
    width: 100%;
  }
}
</style>
