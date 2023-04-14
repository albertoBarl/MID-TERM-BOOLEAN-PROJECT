<template lang="">
  <div class="jumbotron">
    <jumbotron />
  </div>
  <div class="artistcoachSect">
    <artistcoachSect />
  </div>
  <div class="testimonials">
    <testimonials />
  </div>
  <div class="onlinecourses">
    <onlinecourses />
  </div>
  <div class="articles">
    <articles />
  </div>
  <div class="upcoming">
    <upcoming />
  </div>
</template>
<script>
import jumbotron from "./elements/jumbotron.vue";
import artistcoachSect from "./elements/artistcoachSect.vue";
import testimonials from "./elements/testimonials.vue";
import onlinecourses from "./elements/onlinecourses.vue";
import articles from "./elements/articles.vue";
import upcoming from "./elements/upcoming.vue";

export default {
  components: {
    jumbotron,
    artistcoachSect,
    testimonials,
    onlinecourses,
    articles,
    upcoming,
  },
};
</script>
<style lang="scss" scoped>
@use "../styles/generals.scss" as *;
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.artistcoachSect,
.onlinecourses,
.upcoming {
  padding: 75px;
}
.testimonials,
.articles {
  padding: 75px;
  background-color: $d-wall;
}
</style>
