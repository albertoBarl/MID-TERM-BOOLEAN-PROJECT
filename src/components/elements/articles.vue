<template lang="">
  <div class="container d-flex flex-column align-items-center">
    <div class="pCenter">
      <h2>Articles and Tips</h2>
      <h3>Latest From the Blog</h3>
    </div>

    <!-- content -->
    <div class="articles">
      <div
        class="carta"
        v-for="(item, index) in articles"
        :class="[index] == 0 ? 'spCarta' : ''"
      >
        <div>
          <img
            :src="`src/assets/images/${articles[index].image}`"
            alt="not available"
          />
        </div>
        <div class="description">
          <p>{{ articles[index].type }}</p>
          <h5>{{ articles[index].label }}</h5>
          <span
            >{{ articles[index].date }} {{ articles[index].views }}views</span
          >
        </div>
      </div>
    </div>

    <!-- footer -->
    <div></div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      articles: [
        {
          image: "artist-blog-02-500x680.jpg",
          type: "ARTIST",
          label: "Connection Between Self-Portraits and Identity",
          date: "May 15, 2020",
          views: "1,689",
        },
        {
          image: "artist-blog-03-480x356.jpeg",
          type: "ARTIST",
          label: "Brush Strokes Energize Trees in Paintings",
          date: "May 15, 2020",
          views: "1,628",
        },
        {
          image: "artist-blog-01-480x356.jpg",
          type: "ARTIST",
          label: "Pocket-Sized Notebooks Hold Miniature Paintings",
          date: "May 15, 2020",
          views: "1,513",
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

.articles {
  padding: 75px;
  display: flex;
  align-items: flex-start;
  gap: 25px;
  .carta {
    background-color: white;
    width: 250px;
    img {
      width: 100%;
    }
    .description {
      padding: 25px;
      line-height: 2.5;
    }
  }

  .spCarta {
    position: relative;
    background-color: white;
    width: 400px;
    img {
      width: 100%;
      height: 100%;
    }
    .description {
      z-index: 3;
      position: absolute;
      top: 0;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.2);
      color: white;
      display: flex;
      flex-direction: column;
      justify-content: end;
      padding: 34px;
      line-height: 3;
    }
  }
}
</style>
