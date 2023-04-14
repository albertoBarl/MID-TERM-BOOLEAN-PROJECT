<template lang="">
  <div class="container d-flex justify-content-center gap-4 p-3">
    <span>Starts TOMORROW! Our biggest event of the year...</span>
    <div></div>
    <button class="btn">Get ticket</button>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
@use "../../styles/generals.scss" as *;
@use "../../styles/partials/mixins" as *;
@use "../../styles/partials/variables" as *;

.btn {
  padding: 3px 40px;
  background-color: $aranciata;
  color: $wall;
  &:hover {
    background-color: $cielo;
    color: $wall;
  }
}
</style>
