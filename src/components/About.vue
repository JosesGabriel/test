<template>
  <section class="flex description__section">
    <img class="me" src="../assets/images/ses2.png" />
    <span class="description__heading"
      >Hello, I'm <span class="secondary--text">Joses.</span></span
    >
    <div class="description__body">
      I'm a developer with an affinity towards Front End Development but can
      switch to Back End when the need arises.
    </div>
    <br />
    <div class="description__body">
      I have participated in Programming competitions (once outside the
      country!) and eventually grew to judge a few. I've spoken at technical
      conferences and loved it so much that I also teach programming at
      <a href="https://mcm.edu.ph/" target="#">Malayan College Mindanao</a>.
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
.description__heading {
  font-weight: bold;
  font-size: 2.1em;
}
.description__body {
  width: 35vw;
  text-align: center;
}
.me {
  width: 200px;
  padding-bottom: 20px;
}
</style>
