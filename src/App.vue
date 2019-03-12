<template>
  <div id="app">
    <div id="nav">
      <ul id="menu">
        <router-link to="/">
          <li @click="toggleMenu()">Strona główna</li>
        </router-link>
        <router-link v-for="i in 9" :key="i" :to="`/poem/${i}`">
          <li @click="toggleMenu()">{{ titles[i - 1] }}</li>
        </router-link>
      </ul>
      <div @click="toggleMenu()" id="hamburger-menu">
        <span></span>
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>
    <router-view/>
  </div>
</template>

<script>
export default {
  data() {
    return {
      titles: [
        "Cisza Morska",
        "Z podań żeglarskich",
        "Śpiew morza",
        "Mewy",
        "Znad morza",
        "Morze wracające",
        "Gwiazdy",
        "Morze przesadne",
        "Bałtyk"
      ]
    };
  },
  methods: {
    toggleMenu() {
      document.getElementById("hamburger-menu").classList.toggle("open");
      document.getElementById("menu").classList.toggle("show");
    }
  }
};
</script>

<style lang="scss">
* {
  margin: 0;
}

body {
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px 0;
  height: 40px;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 100;
  background-color: white;
  width: 100vw;
  max-width: 100%;
  box-shadow: 0 0 10px #000;

  ul {
    list-style-type: none;
    width: 100vw;
    position: absolute;
    left: 0;
    margin: 0;
    padding: 0;

    a {
      display: inline-block;
      padding: 10px;
      text-transform: uppercase;
      text-decoration: none;
      border-right: 1px dashed black;
      font-weight: bold;
      color: #2c3e50;
      font-size: 14.5px;
      transition: 0.25s ease-in-out;

      &:first-of-type {
        border-left: 1px dashed black;

        &.router-link-exact-active,
        &:hover {
          border-left: 1px dashed white;
        }
      }

      &.router-link-exact-active,
      &:hover {
        color: #42b983;
        box-shadow: 0px 1px 1px #000, 0px -1px 1px #000;
        border-right: 1px solid white;
      }
    }
  }
  #hamburger-menu {
    display: none;
    position: fixed;
    right: 10px;
    top: 10px;
    width: 60px;
    height: 45px;
    transform: rotate(0deg);
    transition: 0.5s ease-in-out;
    cursor: pointer;

    span {
      display: block;
      position: absolute;
      height: 9px;
      width: 100%;
      background: #2c3e50;
      border-radius: 9px;
      opacity: 1;
      left: 0;
      transform: rotate(0deg);
      transition: 0.25s ease-in-out;
      border: 2px solid #fff;

      &:nth-child(1) {
        top: 0px;
      }

      &:nth-child(2),
      &:nth-child(3) {
        top: 18px;
      }

      &:nth-child(4) {
        top: 36px;
      }
    }

    &.open span {
      background: #fff;

      &:nth-child(1) {
        top: 18px;
        width: 0%;
        left: 50%;
      }

      &:nth-child(2) {
        transform: rotate(45deg);
      }

      &:nth-child(3) {
        transform: rotate(-45deg);
      }

      &:nth-child(4) {
        top: 18px;
        width: 0%;
        left: 50%;
      }
    }
  }
}

@media screen and (max-width: 1360px) {
  #nav {
    padding: 30px;
    height: 40px;
    position: fixed;
    top: 0;
    left: 0;
    z-index: 1;
    background-color: transparent;
    width: 100vw;
    box-shadow: none;

    #menu {
      position: fixed;
      top: 0;
      left: calc(100vw);
      height: 100vh;
      width: 300px;
      background: white;
      display: flex !important;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      opacity: 0;
      background: #2c3e50;
      transition: 0.25s ease-in-out;

      &.show {
        opacity: 1;
        left: calc(100vw - 300px);
        z-index: 2;
      }

      a {
        display: block;
        padding: 10px;
        text-transform: uppercase;
        text-decoration: none;
        border-right: none;
        font-weight: bold;
        color: white;
        font-size: 14.5px;

        &.router-link-exact-active,
        &:hover {
          color: #42b983;
        }

        &:first-of-type {
          border-left: none;
        }
      }
    }
    #hamburger-menu {
      display: block;
      z-index: 2;
    }
  }
}
</style>
