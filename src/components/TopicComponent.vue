<template>
  <div class="title">
      <main>
        <h1>{{ title }}</h1>
      </main>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "topic",
  props: {
      title: String
  }
};
</script>

<style lang="scss" scoped>
    h1{
        position: absolute;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        margin: auto;
        display: block;
        z-index: 1;
        height: 5vw;
        font-size: 4vw;
        width: 80vw;
        color: white;
        text-shadow: 0 0 10px #000,
                    5px 5px 10px #000,
                    -5px 5px 10px #000,
                    5px -5px 10px #000,
                    -5px -5px 10px #000,
    }
</style>
