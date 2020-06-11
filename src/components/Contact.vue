<template>
  <section class="flex contact__section">
    <span class="contact__heading">
      CONTACT
    </span>
    <span class="contact__subheading">
      Have a question or interested in working together?
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
    <span class="contact__credits">JOSES GABRIEL LU © 2020</span>
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
  height: 100%;
  outline: none;
  margin: 10px 15px;
}
.contact__button:hover {
  opacity: 0.5;
}
.contact__credits {
  margin: 25px 0;
  font-size: 1.3em;
}
@media screen and (max-width: 768px) {
  .contact__subheading {
    font-size: 1.3em;
  }
  .contact__button img {
    width: 35px;
  }
}
</style>
