<template lang="">
  <div class="container-fluid d-flex flex-column align-items-center">
    <div class="pCenter">
      <h2>Testimonials</h2>
      <h3>Why do people love me?</h3>
    </div>
    <div>
      <div class="slider">
        <div class="item-slider" v-for="(item, index) in slider">
          <div
            class="item"
            :class="index === activeImage ? 'active' : ''"
            @click="switchImg(index)"
          >
            <h6>{{ slider[index].ref }}</h6>
            <p class="mt-3">{{ slider[index].inside }}</p>
            <div class="d-flex align-items-center mt-3">
              <img
                :src="`src/assets/images/${slider[index].avatar}`"
                alt="avatar"
                class="rounded-circle"
              />

              <div class="ms-3">
                <h6>{{ slider[index].owner }}</h6>
                <span>/ {{ slider[index].job }}</span>
              </div>
            </div>
          </div>
        </div>
      </div>
      <!--Pulsanti di navigazione prec e succ del carosello immagini-->
      <div class="circles-container">
        <div
          class="circle"
          v-for="(item, index) in slider"
          :class="index === activeImage ? 'active' : ''"
          @click="switchImg(index)"
        ></div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      activeImage: 0,
      slider: [
        {
          ref: "High level of efficiency and scientific teaching methods",
          inside:
            "I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.",
          avatar: "artist-testimonial-avatar-04.jpg",
          owner: "Mina Hollace",
          job: "Freelancer",
        },
        {
          ref: "Professional team of specialists and passionate mentors at reach",
          inside:
            "I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.				",
          avatar: "artist-testimonial-avatar-01.jpg",
          owner: "Madley Pondor",
          job: "IT Specialist",
        },
        {
          ref: "The MaxCoach team works really hard to ensure high quality",
          inside:
            "I am happy with their arrangement of lessons and subjects. They reflect a scientific  investigation into effective methods to be adopted for learners of all levels.				",
          avatar: "artist-testimonial-avatar-03.jpg",
          owner: "Luvic Dubble",
          job: "Private Tutor",
        },
        {
          ref: "It's a choice of quality for people with special needs",
          inside:
            "I'm a very strict person so I require everything to be organized and neat. Then, I'll be able to make things right and shine. MaxCoach guys just got me.				",
          avatar: "artist-testimonial-avatar-02.jpg",
          owner: "Florence Themes",
          job: "Multimedia Admin",
        },
      ],
    };
  },
  methods: {
    switchImg(index) {
      this.activeImage = index;
    },
  },
};
</script>
<style lang="scss" scoped>
@use "../../styles/generals.scss" as *;
@use "../../styles/partials/mixins" as *;
@use "../../styles/partials/variables" as *;

.pCenter {
  display: flex;
  flex-direction: column;
  align-items: center;
  h3 {
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

.slider {
  margin: 50px 0px;
  padding: 25px;
  display: flex;
  gap: 25px;
  width: 90vw;
  position: relative;
  overflow: auto;
}

.item {
  opacity: 0.1;
  height: 100%;
  min-width: calc(100% / 4);
  background-color: $wall;
  padding: 34px;
  img {
    width: 50px;
  }
}

.item.active {
  opacity: 1;
}

.circles-container {
  display: flex;
  justify-content: center;
}

.circle {
  display: inline-block;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background-color: rgba(174, 174, 174, 0.509);
  margin: 10px;
  cursor: pointer;
}

.circle.active,
.circle:hover {
  background-color: rgba(174, 174, 174, 1);
}

.hidden {
  display: none;
}
</style>
