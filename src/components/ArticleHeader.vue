<template>
  <div id="article-header">
    <h2>{{ titles[articleId - 1] }}</h2>
  </div>
</template>

<script>
export default {
  name: "ArticleHeader",
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
  props: {
    articleId: Number(String)
  }
};
</script>
