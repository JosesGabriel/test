<template>
  <section class="flex contact__section">
    <span class="contact__heading">
      CONTACT
    </span>
    <span class="contact__subheading">
      Have a question or interested in working together? You can find me here:
    </span>
    <div>
      <a
        href="https://www.linkedin.com/in/joses-gabriel-lu-660a92163/"
        target="#"
        class="contact__button"
      >
        <img src="../assets/images/icons/linkedin.svg" width="45px" />
      </a>
      <a
        href="https://github.com/JosesGabriel"
        target="#"
        class="contact__button"
      >
        <img src="../assets/images/icons/github.svg" width="45px" />
      </a>
      <a
        href="mailto:josesgabriellu@gmail.com"
        target="#"
        class="contact__button"
      >
        <img src="../assets/images/icons/email.png" width="45px" />
      </a>
    </div>
  </section>
</template>

<style scoped>
.contact__heading {
  margin: 2.5vh 0;
  font-size: 2.5em;
  font-weight: bold;
  text-decoration: underline;
}
.contact__subheading {
  font-size: 1.6em;
  margin-bottom: 2vh;
}
.contact__button {
  background: none;
  border: none;
  padding: 6px;
  /* border-radius: 100%; */
  height: 100%;
  outline: none;
  margin: 10px 15px;
}
</style>
