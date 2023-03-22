<template>
  <section class="flex description__section">
    <img class="me" loading="lazy" src="../assets/images/ses2.png" />
    <span class="description__heading">Hello, I'm Joses.</span>
    <div class="description__body">
      <br />
      I am a Software Engineer with 6 years of professional experience and a
      demonstrated history of leadership and working in the software development
      industry.
    </div>
    <br />
    <div class="description__body">
      I am currently the COO of
      <a
        class="nuxify__link nuxify__about"
        href="https://nuxify.tech/"
        target="_blank"
        >Nuxify</a
      >, a development-as-a-service (DaaS) company based in the Philippines.
      <br /><br />

      I specialize in Mobile Development where I build apps using
      <img class="icon" loading="lazy" src="../assets/icons/dart.png" /> Dart &
      <img class="icon" loading="lazy" src="../assets/icons/flutter.png" />
      Flutter. <br /><br />
      I also work in the Frontend with Web using
      <img class="icon" loading="lazy" src="../assets/icons/vue.png" />
      Vue.js/
      <img class="icon" loading="lazy" src="../assets/icons/nuxt.png" /> Nuxt,
      <img class="icon" loading="lazy" src="../assets/icons/javascript.png" />
      Javascript/
      <img class="icon" loading="lazy" src="../assets/icons/typescript.png" />
      Typescript, and
      <img class="icon" loading="lazy" src="../assets/icons/node.png" /> Node.
      <br />
      <br />

      I occasionally accept speaking engagements with conferences and
      universities to speak about the world of tech.
    </div>
  </section>
</template>

<style scoped>
.flex {
  justify-content: unset;
}
.description__section {
  padding-top: 40px;
  font-size: 2em;
  margin-bottom: 80px;
}
.nuxify__about {
  color: white;
  text-decoration: underline;
}
.description__heading {
  font-weight: 900;
  font-size: 2.1em;
  color: white;
  background-image: linear-gradient(to right, #ac43cf, #b44d85);
  border-radius: 5px;
  display: inline;
  padding-left: 20px;
  padding-right: 20px;
  margin-bottom: 10px;
}
.description__body {
  width: 35vw;
  text-align: center;
  color: #a1a1a1;
}
.me {
  width: 200px;
  padding-bottom: 20px;
}
.icon {
  width: 15px;
}
@media screen and (max-width: 768px) {
  .description__body {
    width: 60vw;
  }
}
@media screen and (max-width: 480px) {
  .description__body {
    width: 70vw;
  }
}
</style>
