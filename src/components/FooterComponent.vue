<template>
  <div>
    <p>{{ authors }} &copy Wszelkie prawa zastrzeżone</p>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "pageFooter",
  props: {
      authors: String
  }
};
</script>

<style lang="scss" scoped>
    p{
        position: absolute;
        right: 10px;
        bottom: 10px;
        display: block;
        z-index: 2;
        height: auto;
        font-size: 1em;
        width: 50vw;
        color: white;
        text-align: right;
        text-shadow: 0 0 10px #000,
                    2px 2px 3px #000,
                    -2px 2px 3px #000,
                    2px -2px 3px #000,
                    -2px -2px 3px #000,
    }
</style>
