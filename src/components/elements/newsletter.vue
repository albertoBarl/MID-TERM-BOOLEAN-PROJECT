<template lang="">
  <div class="container">
    <div class="row">
      <div class="col-3">
        <h2 class="text-white text-end">Newsletter to get in touch</h2>
      </div>
      <div class="col-9">
        <div class="pInput d-flex">
          <input
            class="form-control text-white"
            type="text"
            name=""
            id=""
            placeholder="Your e-mail"
          />
          <button type="submit" class="btn bg-none fs-1 text-white">
            &rarr;
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
@use "../../styles/generals.scss" as *;
@use "../../styles/partials/mixins" as *;
@use "../../styles/partials/variables" as *;

.pInput {
  border-bottom: 3px solid rgba(255, 255, 255, 0.5);
  &:hover {
    border-bottom: 3px solid white;
  }
  .form-control {
    background: none;
    border: none;
  }
}
</style>
