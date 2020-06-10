<template>
  <div id="app">
    <SplashView />
    <About />
    <Showcase />
    <Contact />
  </div>
</template>

<script>
import SplashView from "./components/SplashView.vue";
import About from "./components/About.vue";
import Showcase from "./components/Showcase.vue";
import Contact from "./components/Contact.vue";

export default {
  name: "App",
  components: {
    SplashView,
    About,
    Showcase,
    Contact,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Karla&family=Noto+Sans+JP:wght@100&display=swap");
html {
  max-width: 100%;
  overflow-x: hidden;
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
