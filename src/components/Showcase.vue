<template>
  <section :style="'background-color: ' + project.background">
    <div class="project__card">
      <div class="showcase__images">
        <div
          class="showcase__container"
          :class="project.image[1] ? 'showcase__container--main' : ''"
        >
          <img
            class="showcase__image"
            :src="project.image[0]"
            loading="lazy"
            @click="index = 0"
          />
          <img
            v-if="project.isMobile"
            class="showcase__image"
            :src="project.image[1]"
            loading="lazy"
            @click="index = 0"
          />
        </div>
        <vue-gallery-slideshow
          :images="project.image"
          :index="index"
          @close="index = null"
        ></vue-gallery-slideshow>
      </div>
      <div class="showcase__text">
        <div class="showcase__heading">
          {{ project.name }}
        </div>
        <br />
        <br />
        <div class="showcase__details">
          {{ project.description }}
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import VueGallerySlideshow from "vue-gallery-slideshow";
export default {
  components: {
    VueGallerySlideshow,
  },
  props: {
    project: Object,
  },
  data() {
    return {
      index: null,
    };
  },
};
</script>

<style scoped>
.showcase__container {
  display: inline-flex;
  border-radius: 8px;
  box-shadow: 0 5px 5px 0 rgba(84, 88, 90, 0.5), 0 0 0 1px #ffffff;
  margin: 50px 0;
  transition: 0.2s linear;
  background-color: white;
}
.showcase__container--main {
  z-index: 2;
}
.showcase__container--secondary {
  right: 5vw;
}
.showcase__container--secondary img {
  height: 250px;
}
.showcase__images {
  display: inline-flex;
  justify-content: center;
  width: 100%;
}
.showcase__image {
  max-width: 31vw;
  height: 300px;
  background-size: cover;
  cursor: pointer;
  margin: 5px;
  border-radius: 3px;
  object-fit: cover;
  filter: drop-shadow(2px 4px 6px black);
}
.showcase__container:hover {
  box-shadow: 0px 14px 29px 5px rgba(156, 157, 161, 0.468), 0 0 0 4px #e871d6d8;
  z-index: 2;
}
.showcase__text {
  text-align: center;
}
.showcase__heading {
  font-size: 3em;
  margin-bottom: 2vh;
  color: white;
  background-image: linear-gradient(to right, #ac43cf, #b44d85);
  border-radius: 5px;
  display: initial;
  font-weight: 900;
  padding-left: 20px;
  padding-right: 20px;
  margin-bottom: 10px;
}
.showcase__details {
  display: inline-flex;
  font-size: 1.9em;
  color: #a1a1a1;
  width: 35vw;
  text-align: center;
  margin-bottom: 7vh;
}
@media screen and (max-width: 768px) {
  .showcase__details {
    width: 60vw;
  }
  .showcase__container {
    padding: 10px;
  }
  .showcase__container--main {
    left: 0;
  }
  .showcase__container--secondary {
    display: none;
  }
  .showcase__image {
    max-width: unset;
    height: 20vh;
  }
}
@media screen and (max-width: 480px) {
  .showcase__details {
    width: 70vw;
  }
}
</style>
