<template>
  <section class="flex description__section">
    <img class="me" loading="lazy" src="../assets/images/ses2.png" />
    <span class="description__heading">Hello, I'm Joses.</span>
    <div class="description__body">
      I'm a software engineer with an affinity towards Mobile and Web
      Development.
    </div>
    <br />
    <div class="description__body">
      Currently the COO of
      <a
        class="nuxify__link nuxify__about"
        href="https://nuxify.tech/"
        target="_blank"
        >Nuxify</a
      >, a software development company based in the Philippines. <br /><br />

      I have participated in programming competitions (once outside the
      country!) and eventually grew to judge a few. I am also frequently
      commissioned to speak at conferences and colleges to speak about tech.
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
