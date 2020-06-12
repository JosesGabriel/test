<template>
  <section class="" :style="'background-color: ' + project.background">
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
      </div>
      <vue-gallery-slideshow
        :images="project.image"
        :index="index"
        @close="index = null"
      ></vue-gallery-slideshow>
      <div
        class="showcase__container"
        :class="project.image[1] ? 'showcase__container--secondary' : ''"
        v-if="project.image[1]"
      >
        <img
          class="showcase__image"
          :src="project.image[1]"
          loading="lazy"
          @click="index = 1"
        />
      </div>
    </div>
    <div class="showcase__text">
      <div class="showcase__heading">{{ project.name }}</div>
      <div class="showcase__details">{{ project.description }}</div>
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
  background-color: #f5f5f5;
  padding: 15px;
  border-radius: 8px;
  box-shadow: 0 5px 5px 0 rgba(84, 88, 90, 0.5), 0 0 0 1px #e6ecf8;
  position: relative;
  margin: 50px 0;
  margin-top: 15vh;
  text-align: center;
  height: 100%;
  /* transition: 0.4s; */
  /* Enable hardware acceleration to fix laggy transitions */
  /* -webkit-transform: none;
  transform: none; */
  transition: 0.4s linear;
}
.showcase__container--main {
  z-index: 2;
  left: 11vw;
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
}
.showcase__container:hover {
  box-shadow: 2px 14px 29px 0px rgba(42, 44, 51, 1);
  z-index: 2;
}
.showcase__text {
  text-align: center;
}
.showcase__heading {
  font-weight: bolder;
  font-size: 3em;
  margin-bottom: 2vh;
  color: white;
}
.showcase__details {
  display: inline-flex;
  font-size: 1.9em;
  color: white;
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
