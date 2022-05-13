<template>
  <section class="flex header__section">
    <header class="header">
      <div class="header--name">JGL</div>
      <div>
        <button
          @click="toggleMobileMenu = !toggleMobileMenu"
          class="header__button--mobile"
        >
          <img src="../assets/images/icons/menu.svg" width="30px" />
        </button>
      </div>
    </header>

    <div class="header__container--mobile" v-if="toggleMobileMenu">
      <a href="#splash" @click="toggleMobileMenu = false">Home</a>
      <a href="#about" @click="toggleMobileMenu = false">About</a>
      <a href="#showcase" @click="toggleMobileMenu = false">Projects</a>
      <a href="#contact" @click="toggleMobileMenu = false">Contact</a>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      toggleMobileMenu: false,
    };
  },
};
</script>

<style scoped>
.header__section {
  background-color: #000000;
  position: fixed;
  width: 100%;
  z-index: 3;
}
.header {
  display: flex;
  justify-content: space-between;
  padding-top: 1vh;
  width: 100%;
}
.header--name {
  font-size: 2em;
  margin-left: 2vw;
  margin-top: 2vh;
  color: #fff;
}
.header__nav {
  font-size: 1.8em;
  color: white;
  margin-left: 2vw;
}
.header__nav--link {
  text-decoration: none;
  color: white;
  margin: 10px;
  text-transform: uppercase;
}
.header__nav--link:hover {
  background-color: white;
  color: #21384a;
  padding: 5px;
  border-radius: 10px;
}
.header__socials {
  margin-right: 2vw;
}
.header__socials--link:hover {
  opacity: 0.4;
}
.header__socials--link {
  margin-left: 10px;
}
.header__socials--link img,
.header__button--mobile img {
  filter: invert(1);
}
.header__button--mobile {
  background-color: transparent;
  border: 0;
  outline: none;
}
.header__container--mobile {
  font-size: 1.8em;
  width: 100%;
  background-color: #333;
}
.header__container--mobile a {
  display: block;
  color: white;
  padding: 10px;
  text-transform: uppercase;
}

/* @media screen and (max-width: 600px) {
  .header {
    display: none;
  }
  .header--mobile {
    display: flex;
    justify-content: flex-end;
    width: 100%;
    border-bottom: 1px solid white;
  }
} */
</style>
