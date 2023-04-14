<template lang="">
  <div class="container-fluid">
    <div class="pCenter">
      <h2>Artist coaching</h2>
      <h3>Latest Online Courses</h3>
    </div>

    <!-- course list -->
    <div class="courses">
      <div class="card" v-for="(item, index) in cards">
        <div>
          <img
            :src="`src/assets/images/${cards[index].image}`"
            alt="not available"
          />
        </div>
        <p>${{ cards[index].price }}</p>
        <h5>{{ cards[index].label }}</h5>
        <span
          >{{ cards[index].nLessons }} Lessons
          {{ cards[index].nStudents }} Students</span
        >
      </div>
      <button class="btn">View all courses &rarr;</button>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      cards: [
        {
          image: "artist-course-01-480x480.jpg",
          price: "18.00",
          label: "The Acrylic Painting Academy",
          nLessons: "4",
          nStudents: "50",
        },
        {
          image: "artist-course-02-480x480.jpg",
          price: "21.00",
          label: "Drawing adn Shading: Complete Course",
          nLessons: "14",
          nStudents: "50",
        },
        {
          image: "artist-course-03-480x480.jpg",
          price: "19.00",
          label: "The Color Theory for Digital Artist",
          nLessons: "7",
          nStudents: "50",
        },
        {
          image: "artist-course-04-480x480.jpg",
          price: "35.00",
          label: "Ultimate Guide to Digital Sketching for Beginner",
          nLessons: "14",
          nStudents: "50",
        },
        {
          image: "artist-course-05-480x480.jpg",
          price: "19.00",
          label: "Portrait Drawing The Smart Way",
          nLessons: "2",
          nStudents: "50",
        },
        {
          image: "artist-course-06-480x480.jpg",
          price: "19.00",
          label: "Mastering Watercolor Painting from Beginner",
          nLessons: "9",
          nStudents: "50",
        },
        {
          image: "artist-course-07-480x480.jpg",
          price: "25.00",
          label: "The Art & Science of Drawing",
          nLessons: "4",
          nStudents: "50",
        },
        {
          image: "artist-course-08-480x480.jpg",
          price: "22.00",
          label: "The Colored Pencil Drawing Course",
          nLessons: "6",
          nStudents: "50",
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
.pCenter {
  display: flex;
  flex-direction: column;
  align-items: center;
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

.courses {
  display: flex;
  flex-wrap: wrap;
  gap: 50px;
  justify-content: center;
  margin-top: 75px;
  .card {
    width: calc(75% / 4);
    border: none;
    &:hover {
      padding: 10px;
      border: 1px solid black;
      border-radius: 0;
    }
    img {
      width: 100%;
    }
    p {
      color: $aranciata;
    }
  }
}

.btn {
  margin-top: 50px;
  padding: 10px 30px;
  background-color: $aranciata;
  color: $wall;
  &:hover {
    background-color: $cielo;
    color: $wall;
  }
}
</style>
