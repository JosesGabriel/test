<template>
  <section class="flex showcase__section">
    <div class="card showcase__container">
      <div class="showcase__heading">Projects</div>
      <section v-for="(project, i) in projects" :key="i">
        <div v-if="currentVisibleProject == i">
          <div class="showcase__subtitle">
            <button
              v-if="currentVisibleProject > 0"
              type="button"
              class="showcase__button showcase__button--next"
              @click="currentVisibleProject--"
            >
              <img
                src="../assets/images/icons/right-arrow.png"
                width="25px"
                class="img_flip"
              />
            </button>
            <a :href="project.link" target="#">{{ project.name }}</a>
            <button
              type="button"
              class="showcase__button"
              @click="detailsToggle = !detailsToggle"
            >
              <img src="../assets/images/icons/info.svg" width="80%" />
            </button>
            <button
              v-if="currentVisibleProject < projects.length - 1"
              type="button"
              class="showcase__button showcase__button--next"
              @click="currentVisibleProject++"
            >
              <img src="../assets/images/icons/right-arrow.png" width="25px" />
            </button>
          </div>
          <div v-if="detailsToggle" class="showcase__details">
            <span>{{ project.description }}</span
            ><br /><br />
            <span>
              {{ project.sub_description }}
            </span>
          </div>
          <div v-else>
            <img
              class="image"
              v-for="(image, i) in project.images"
              :src="image"
              :key="i"
              @click="index = i"
            />
            <vue-gallery-slideshow
              :images="project.images"
              :index="index"
              @close="index = null"
            ></vue-gallery-slideshow>
          </div>
        </div>
      </section>
    </div>
  </section>
</template>

<script>
import VueGallerySlideshow from "vue-gallery-slideshow";

export default {
  data() {
    return {
      currentVisibleProject: 0,
      projects: [
        {
          name: "Lyduz / Arbitrage Philippines",
          link: "https://lyduz.com",
          description:
            "My biggest project to date, where I led the frontend team in development. VueJS was the framework of choice and I handled the initialization of the entire frontend codebase and planned the infrastructure, including what standards would be enforced and the surrounding implementation of the website.",
          sub_description:
            "The platform was in the financial technology industry where we dealt with everything related to the Philippine Stock Exchange. It was a multi-faceted site with many different components including a built-in social media platform, charting tools, real-time trading data, trading journals and much more.",
          images: [
            require("../assets/images/projects/lyduz/social_dark.png"),
            require("../assets/images/projects/lyduz/watchlist_dark.png"),
            require("../assets/images/projects/lyduz/chart_dark.png"),
            require("../assets/images/projects/lyduz/landing_page.png"),
            require("../assets/images/projects/lyduz/profile_light.png"),
            require("../assets/images/projects/lyduz/watchlist_light.png"),
          ],
        },
        {
          name: "Vyndue",
          link: "https://vyndue.com",
          description:
            "A chat client I built for the Philippines Stock Trading Community. Written using Vue/Nuxt.",
          sub_description:
            "This chat client was built on top of the Matrix protocol. A new standard for open, decentralised communication.",
          images: [
            require("../assets/images/projects/knocc/default.png"),
            require("../assets/images/projects/knocc/explore-rooms.png"),
          ],
        },
        {
          name: "Boomity",
          link: "https://boomity.com",
          description:
            "I was part of the development team of Boomity when I was doing freelance work.",
          sub_description:
            "BOOMITY's an easy to manage web marketing platform, customized specifically to users needs. A content management system.",
          images: [require("../assets/images/projects/boomity/home.png")],
        },
        {
          name: "Maata Games BV",
          link: "http://www.erectus.world",
          description:
            "Worked in Maata Games where I handled most of the front-end tasks including, but not limited to, translation of designs to fully functional aspects of the software.",
          sub_description:
            "The game we were developing was web based so most of the experience I acquired was web related in the lieu of front end development.",
          images: [
            require("../assets/images/projects/maata/erectus1.jpg"),
            require("../assets/images/projects/maata/erectus2.jpg"),
            require("../assets/images/projects/maata/erectus3.jpg"),
          ],
        },
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
.img_flip {
  -webkit-transform: scaleX(-1);
  transform: scaleX(-1);
}
.showcase__section {
  background-color: #7dcc93;
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
  color: black;
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
.showcase__button {
  background: none;
  border: none;
  padding: 0;
  border-radius: 20px;
  height: 100%;
  outline: none;
}
.showcase__button:hover,
.showcase__button:focus {
  opacity: 0.2;
}
.showcase__button--next {
  vertical-align: middle;
}
.showcase__details {
  font-size: 1.4em;
}
</style>
