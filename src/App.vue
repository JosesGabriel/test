<template>
  <div id="app">
    <Header />
    <SplashView id="splash" />
    <About id="about" />
    <Showcase
      v-for="(project, i) in projects"
      :key="i"
      :project="project"
      id="showcase"
    />
    <Contact id="contact" />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import SplashView from "./components/SplashView.vue";
import About from "./components/About.vue";
import Showcase from "./components/Showcase.vue";
import Contact from "./components/Contact.vue";

export default {
  name: "App",
  components: {
    Header,
    SplashView,
    About,
    Showcase,
    Contact,
  },
  data() {
    return {
      projects: [
        {
          name: "Lyduz / Arbitrage Philippines",
          description:
            "My biggest project to date, where I led the frontend team in development. The platform was in the financial technology industry where we dealt with everything related to the Philippine Stock Exchange. It was a multi-faceted site with many different components including a built-in social media platform, charting tools, real-time trading data, trading journals and much more.",
          image: [
            require("./assets/images/projects/lyduz/chart_light.png"),
            require("./assets/images/projects/lyduz/chart_dark.png"),
            require("./assets/images/projects/lyduz/landing_page.png"),
            require("./assets/images/projects/lyduz/profile_light.png"),
            require("./assets/images/projects/lyduz/social_dark.png"),
            require("./assets/images/projects/lyduz/watchlist_dark.png"),
            require("./assets/images/projects/lyduz/watchlist_light.png"),
          ],
          background: "#7dcc93",
        },
        {
          name: "Vyndue",
          description:
            "A chat client for the Philippine Stock Trading Community I built when working for Lyduz. This was built on top of the Matrix protocol, a new standard for open, decentralised communication.",

          image: [
            require("./assets/images/projects/knocc/default.png"),
            require("./assets/images/projects/knocc/explore-rooms.png"),
          ],
          background: "#14476b",
        },
        {
          name: "Boomity",
          description:
            "BOOMITY is an easy to manage web marketing platform, customized specifically to users needs.",
          image: [require("./assets/images/projects/boomity/home.png")],
          background: "#e39470",
        },
        {
          name: "Maata Games BV",
          description:
            "Worked in Maata Games where I handled most of the front-end tasks including, but not limited to, translation of designs to fully functional aspects of the software.",
          image: [
            require("./assets/images/projects/maata/erectus2.jpg"),
            require("./assets/images/projects/maata/erectus3.jpg"),
          ],
          background: "#679895",
        },
      ],
    };
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Karla&family=Noto+Sans+JP:wght@100&display=swap");
html {
  max-width: 100%;
  overflow-x: hidden;
  scroll-behavior: smooth;
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-family: "Karla", Avenir, Helvetica, sans-serif;
  line-height: 1.42;
  font-size: 10px;
  color: #545454;
}
a {
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
body {
  margin: 0;
}
.test {
  height: 70vh;
}
.flex {
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
}
.secondary--text {
  color: #7dcc93;
}
</style>
