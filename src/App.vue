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
          background: "#000000",
        },
        {
          name: "CoinMode Wallet",
          description:
            "A digital wallet that supports cryptocurrencies as well as GBP, EUR, and USD. Send and receive payments directly to players, friends and colleagues. Currently available on the App Store and Google Play.",
          image: [
            require("./assets/images/projects/coinmode/1.png"),
            require("./assets/images/projects/coinmode/2.png"),
            require("./assets/images/projects/coinmode/3.png"),
            require("./assets/images/projects/coinmode/4.png"),
            require("./assets/images/projects/coinmode/5.png"),
          ],
          background: "#000000",
          isMobile: true,
        },
        {
          name: "FrontRx",
          description:
            "A project I worked on for Nuxify.tech. A platform for Physicians and Pharmacists alike to share information with each other such as prescriptions.",
          image: [
            require("./assets/images/projects/frontrx/home.png"),
            require("./assets/images/projects/frontrx/login.png"),
            require("./assets/images/projects/frontrx/pharma.png"),
          ],
          background: "#000000",
        },
        {
          name: "C3 Cardiogenic Shock App",
          description:
            "An app for patients to monitor their heart rate and to receive a cardiogenic shock if the heart rate is above a certain threshold. Currently available on the App Store and Google Play.",
          image: [
            require("./assets/images/projects/c3/1.jpg"),
            require("./assets/images/projects/c3/2.jpg"),
            require("./assets/images/projects/c3/3.jpg"),
            require("./assets/images/projects/c3/4.jpg"),
          ],
          background: "#000000",
          isMobile: true,
        },
        {
          name: "Vyndue",
          description:
            "A chat client for the Philippine Stock Trading Community I built when working for Lyduz. This was built on top of the Matrix protocol, a new standard for open, decentralised communication.",

          image: [
            require("./assets/images/projects/knocc/default.png"),
            require("./assets/images/projects/knocc/explore-rooms.png"),
          ],
          background: "#000000",
        },
        {
          name: "Boomity",
          description:
            "I was part of the team that developed BOOMITY, an easy to manage web marketing platform, customized specifically to users needs.",
          image: [require("./assets/images/projects/boomity/home.png")],
          background: "#000000",
        },
        {
          name: "Maata Games BV",
          description:
            "Worked in Maata Games where I handled most of the front-end tasks including translation of designs to fully functional aspects of the software.",
          image: [
            require("./assets/images/projects/maata/erectus2.jpg"),
            require("./assets/images/projects/maata/erectus3.jpg"),
          ],
          background: "#000000",
        },
      ],
    };
  },
};
</script>

<style>
@font-face {
  font-family: poppins-regular;
  src: url("./assets/font/Poppins/Poppins-Regular.ttf");
}
@font-face {
  font-family: poppins-medium;
  src: url("./assets/font/Poppins/Poppins-Medium.ttf");
}
@font-face {
  font-family: poppins-light;
  src: url("./assets/font/Poppins/Poppins-Light.ttf");
}
html {
  max-width: 100%;
  overflow-x: hidden;
  scroll-behavior: smooth;
  background-color: black;
}
body::-webkit-scrollbar {
  width: 5px;
}
body::-webkit-scrollbar-track {
  background: transparent;
}
body::-webkit-scrollbar-thumb {
  background-color: rgba(255, 255, 255, 0.3);
  border-radius: 20px;
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-family: poppins-light;
  line-height: 1.42;
  font-size: 10px;
  color: #545454;
  background-color: black;
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
.flex {
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
}
.secondary--text {
  color: #dd62bca9;
}
</style>
