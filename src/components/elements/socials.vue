<template lang="">
  <div class="socialsLogos d-flex gap-4 mt-4">
    <ul class="list-unstyled" v-for="(item, index) in socialLogos">
      <li>
        <a href="/"><i :class="`${socialLogos[index].icona}`"></i></a>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      socialLogos: [
        { type: "facebook", icona: "fab fa-facebook-square" },
        { type: "twitter", icona: "fab fa-twitter" },
        { type: "instagram", icona: "fab fa-instagram" },
        { type: "linkedin", icona: "fab fa-linkedin" },
      ],
    };
  },
};
</script>
<style lang="scss">
@use "../../styles/generals.scss" as *;
@use "../../styles/partials/mixins" as *;
@use "../../styles/partials/variables" as *;

i {
  font-size: 34px;
  color: grey;
  text-decoration: none;
  &:hover {
    color: $aranciata;
  }
}
</style>
