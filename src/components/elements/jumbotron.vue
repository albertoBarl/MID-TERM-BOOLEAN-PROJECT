<template lang="">
  <div class="pBackground" style="height: 80vh">
    <div class="pCenter">
      <h2>Hello, I'm Matin</h2>
      <h3>Artist Coaching And Mentoring Might Be for You.</h3>
      <button class="btn">Get started today</button>
    </div>
    <div class="showing">
      <img
        id="first"
        src="src/assets/images/artist-hero-image-01.jpg"
        alt="not available"
      />
      <img
        id="second"
        src="src/assets/images/artist-hero-image-02.jpg"
        alt="not available"
      />
      <img
        id="third"
        src="src/assets/images/artist-hero-image-04.jpg"
        alt="not available"
      />
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

.pBackground {
  background-color: $d-wall;
  display: flex;
  position: relative;
  justify-content: center;
  align-items: center;
}

.pCenter {
  display: flex;
  align-items: center;
  flex-direction: column;
  z-index: 3;
  h2 {
    font-family: cursive;
    font-style: italic;
    font-size: 40px;
    color: $cielo;
  }
  h3 {
    width: 75%;
    text-align: center;
    font-weight: 500;
  }
  .btn {
    margin-top: 50px;
    padding: 15px 40px;
    background-color: $aranciata;
    color: $wall;
    &:hover {
      background-color: $cielo;
      color: $wall;
    }
  }
}

.showing {
  position: absolute;
  width: 100%;
  height: 100%;
  img {
    position: absolute;
  }
  #first {
    left: 10%;
    top: 50%;
    z-index: 2;
  }
  #second {
    top: 20%;
    left: 15%;
  }
  #third {
    top: 20%;
    right: 10%;
    z-index: 2;
  }
}
</style>
