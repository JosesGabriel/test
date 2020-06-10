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
html {
  max-width: 100%;
  overflow-x: hidden;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 10px;
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
  color: #ff7844;
}
</style>
