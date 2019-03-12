<template>
  <div id="slideShow">
    <img class="image" src="../assets/screen1.jpg">
    <img class="image" src="../assets/screen2.jpg">
    <img class="image" src="../assets/screen3.jpg">
    <img class="image" src="../assets/screen4.jpg">
    <img class="image current" src="../assets/screen5.jpg">
  </div>
</template>

<script>
export default {
  name: "Slider",
  data() {
    return {
      slider: Object
    }
  },
  mounted() {
    var j = 1;
    var max = document.getElementById("slideShow").childNodes.length;
    this.slider = setInterval(() => {
      if (j > max) j = 1;
      if (j === 1) {
        document
          .getElementById("slideShow")
          .childNodes[max - 1].classList.toggle("current");
      } else {
        document
          .getElementById("slideShow")
          .childNodes[j - 2].classList.toggle("current");
      }
      document
        .getElementById("slideShow")
        .childNodes[j - 1].classList.toggle("current");
      j++;
    }, 3000);
  },
  destroyed() {
    clearInterval(this.slider);
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#slideShow {
  position: relative;

  img {
    position: absolute;
    width: 100vw;
    max-width: 100%;
    height: 100vh;
    left: 0;
    opacity: 0;
  }

  .current {
    opacity: 1;
  }
}

@media screen and (max-width: 1360px) {
#slideShow img {
    height: 100vh;
  }
}
</style>
