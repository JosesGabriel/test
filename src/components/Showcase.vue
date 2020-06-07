<template>
  <section class="flex showcase__section">
    <div class="card showcase__container">
      <div class="showcase__heading">Projects</div>
      <div class="showcase__subtitle">
        <a href="https://lyduz.com" target="#">Lyduz / Arbitrage Philippines</a>
        <button
          type="button"
          class="showcase__button--info"
          @click="detailsToggle = !detailsToggle"
        >
          <img src="../assets/images/icons/info.svg" width="100%" />
        </button>
      </div>
      <div v-if="!detailsToggle">
        <img
          class="image"
          v-for="(image, i) in images"
          :src="image"
          :key="i"
          @click="index = i"
        />
        <vue-gallery-slideshow
          :images="images"
          :index="index"
          @close="index = null"
        ></vue-gallery-slideshow>
      </div>
      <div v-else class="showcase__details">
        <span
          >My biggest project to date, where I led the frontend team in
          development. VueJS was the framework of choice and I handled the
          initialization of the entire frontend codebase and planned the
          infrastructure, including what standards would be enforced and the
          surrounding implementation of the website.</span
        ><br /><br />
        <span>
          The platform was in the financial technology industry where we dealt
          with everything related to the Philippine Stock Exchange. It was a
          multi-faceted site with many different components including a built-in
          social media platform, charting tools, real-time trading data, trading
          journals and much more.
        </span>
      </div>
    </div>
  </section>
</template>

<script>
import VueGallerySlideshow from "vue-gallery-slideshow";

export default {
  data() {
    return {
      images: [
        require("../assets/images/projects/lyduz/social_dark.png"),
        require("../assets/images/projects/lyduz/watchlist_dark.png"),
        require("../assets/images/projects/lyduz/chart_dark.png"),
        require("../assets/images/projects/lyduz/landing_page.png"),
        require("../assets/images/projects/lyduz/profile_light.png"),
        require("../assets/images/projects/lyduz/watchlist_light.png"),
      ],
      index: null,
      detailsToggle: false,
    };
  },
  components: {
    VueGallerySlideshow,
  },
  methods: {
    test() {
      alert("vovo");
    },
  },
};
</script>

<style scoped>
.showcase__section {
  background-color: #ff7844;
}
.showcase__container {
  background-color: white;
  width: 50vw;
  padding: 20px;
  border-radius: 20px;
  box-shadow: 0 5px 5px 0 rgba(233, 240, 243, 0.5), 0 0 0 1px #e6ecf8;
  position: relative;
  bottom: 100px;
  text-align: center;
}
.showcase__heading {
  font-size: 3em;
  font-weight: bold;
  text-decoration: underline;
}
.showcase__subtitle {
  font-size: 2em;
  padding: 10px 0;
}
.image {
  width: 200px;
  height: 200px;
  background-size: cover;
  cursor: pointer;
  margin: 5px;
  border-radius: 3px;
  box-shadow: 0 5px 5px 0 rgba(233, 240, 243, 0.5), 0 0 0 1px #e6ecf8;
  object-fit: cover;
}
.showcase__button--info {
  background: none;
  border: none;
  padding: 0;
  border-radius: 20px;
  height: 100%;
  outline: none;
}
.showcase__button--info:hover,
.showcase__button--info:focus {
  opacity: 0.2;
}
.showcase__details {
  font-size: 1.4em;
}
</style>
