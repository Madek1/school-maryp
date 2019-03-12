<template>
  <div id="article-author">
    <h3>{{ authors[articleId - 1] }}</h3>
  </div>
</template>

<script>
export default {
  name: "ArticleAuthor",
  data() {
    return {
      authors: [
        "Adam Mickiewicz",
        "Kpt. Mariusz Zaruski",
        "Kpt. Mariusz Zaruski",
        "Maria Konopnicka",
        "Kazimierz Przerwa-Tetmajer",
        "Krzysztof Kamil Baczyński",
        "Antoni Słonimski",
        "Leopold Staff",
        "Józef Ignacy Kraszewski"
      ]
    };
  },
  props: {
    articleId: Number(String)
  }
};
</script>
