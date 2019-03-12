<template>
  <div id="article">
    <h2>tytul</h2>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sed omnis labore magnam tempora reiciendis nemo commodi, a asperiores aliquam eveniet quos perspiciatis consequuntur aspernatur nobis temporibus facilis! Dolor, ipsam nam?</p>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sed omnis labore magnam tempora reiciendis nemo commodi, a asperiores aliquam eveniet quos perspiciatis consequuntur aspernatur nobis temporibus facilis! Dolor, ipsam nam?</p>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sed omnis labore magnam tempora reiciendis nemo commodi, a asperiores aliquam eveniet quos perspiciatis consequuntur aspernatur nobis temporibus facilis! Dolor, ipsam nam?</p>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sed omnis labore magnam tempora reiciendis nemo commodi, a asperiores aliquam eveniet quos perspiciatis consequuntur aspernatur nobis temporibus facilis! Dolor, ipsam nam?</p>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sed omnis labore magnam tempora reiciendis nemo commodi, a asperiores aliquam eveniet quos perspiciatis consequuntur aspernatur nobis temporibus facilis! Dolor, ipsam nam?</p>
  </div>
</template>

<script>
export default {
  name: "ArticleComponent"
};
</script>

<style lang="scss" scoped>
#article {
  min-height: 100vh;
  position: absolute;
  top: 100vh;
  left: 0;
  right: 0;
  width: 500px;
  margin: 0 auto;

  p {
    margin: 40px 0;
    text-align: left;

    &::first-letter {
      font-size: 32px;
      margin-left: 30px;
    }
  }
}
</style>

