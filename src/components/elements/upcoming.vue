<template lang="">
  <div class="container">
    <div class="pCenter">
      <h2>Upcoming Events</h2>
      <h3>Let's Work Together</h3>
    </div>

    <!-- events list -->
    <div class="events">
      <div
        v-for="(item, index) in evList"
        class="card"
        :class="[index] >= 2 ? 'flex-row-reverse' : ''"
      >
        <img
          :src="`src/assets/images/${evList[index].image}`"
          alt="not available"
        />
        <div>
          <p>{{ evList[index].date }}</p>
          <h5>{{ evList[index].label }}</h5>
          <span>{{ evList[index].place }}</span>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      evList: [
        {
          image: "artist-event-04-250x300.jpg",
          date: "APR 22, 2021",
          label: "Storytelling Workshop",
          place: "Texas, US",
        },
        {
          image: "artist-event-03-250x300.jpg",
          date: "OCT 10, 2020",
          label: "Painting Art Contest 2020",
          place: "New York, US",
        },
        {
          image: "artist-event-02-250x300.jpg",
          date: "NOV 23, 2020",
          label: "International Art Fair 2020",
          place: "Hamburg, Germany",
        },
        {
          image: "artist-event-01-250x300.jpg",
          date: "DEC 15, 2020",
          label: "Street Performance: Call for Artist",
          place: "Illinois, US",
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

.events {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 50px;
  margin-top: 75px;
  .card {
    display: flex;
    flex-direction: row;
    align-items: center;
    line-height: 3;
    gap: 30px;
    width: calc(90% / 2);
    border: none;
    img {
      width: 250px;
    }
  }
}
</style>
