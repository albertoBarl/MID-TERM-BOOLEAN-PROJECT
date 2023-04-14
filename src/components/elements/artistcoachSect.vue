<template lang="">
  <div class="container d-flex flex-column align-items-center">
    <!-- "helping with" section -->
    <div class="helping">
      <div class="pCenter d-flex flex-column align-items-center">
        <h2>Artist coaching</h2>
        <h3>I understand what it takes to create. I can help you with</h3>
      </div>
      <div
        class="d-flex justify-content-around align-items-center gap-5 p-5 mt-4"
      >
        <div v-for="(item, index) in helping">
          <img
            :src="`src/assets/images/${helping[index].image}`"
            alt="not available"
          />
          <h4>{{ helping[index].label }}</h4>
          <p>{{ helping[index].description }}</p>
        </div>
      </div>
    </div>

    <!-- quote section -->
    <div class="quote">
      <div>
        <h1>
          I coach and mentor visual artists, like you, to Create Like You Mean
          It
        </h1>
        <h2>Martin Garrix</h2>
      </div>
      <div>
        <p>
          As a coach and mentor, my ultimate goal is to motivate visual artists
          toward inspired action. I help you get you back on track to being the
          productive, creative, meaningful and authentic artist you truly want
          to be.I support artists in crafting and living a creative life as well
          as feeling good about themselves and their art. As an artist and an
          educator for nearly 30 years, I understand what it takes to create.
        </p>
        <button class="btn">Get started today</button>
      </div>
    </div>

    <!-- youtube video sect -->
    <div class="video">
      <img
        class="position-relative"
        src="src/assets/images/artist-video-poster.jpg"
        alt="not available"
      />
      <a href=""><i class="fab fa-youtube"></i></a>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      helping: [
        {
          image: "artist-box-image-01.png",
          label: "Online Courses",
          description:
            "Online art coaching now offers youy a very powerful way to redesign your artist mind.",
        },
        {
          image: "artist-box-image-02.png",
          label: "One to One",
          description:
            "Getting the necessary clarity about the current state to help you improve your ability,",
        },
        {
          image: "artist-box-image-03.png",
          label: "Anywhere",
          description:
            "Access to valuable and portable program which allow you to setup and live anywhere you want.",
        },
        {
          image: "artist-box-image-04.png",
          label: "On Time",
          description:
            "Punctuality is our top priority because it's an essential criteria to assess a program quality.",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
@use "../../styles/generals.scss" as *;
@use "../../styles/partials/mixins" as *;
@use "../../styles/partials/variables" as *;

.container {
  gap: 105px;
}

.pCenter,
.quote {
  display: flex;
  justify-content: center;
  h3 {
    width: 75%;
    text-align: center;
    font-weight: 500;
  }
  h2 {
    font-family: cursive;
    font-style: italic;
    font-size: 40px;
    color: $cielo;
  }
}

.video {
  width: 55vw;
  position: relative;
  img {
    position: relative;
    width: 100%;
    height: auto;
  }
  i {
    position: absolute;
    top: 50%;
    left: 47%;
    font-size: 75px;
    color: red;
  }
}

.btn {
  margin-top: 50px;
  padding: 15px 40px;
  background-color: $cielo;
  color: $aranciata;
  &:hover {
    background-color: $aranciata;
    color: $wall;
  }
}
</style>
