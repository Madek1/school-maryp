<template>
  <div class="poem">
    <ArticleHeader :articleId="$route.params.id" />
    <ArticleContent :articleId="$route.params.id" />
    <ArticleAuthor :articleId="$route.params.id" />
  </div>
</template>

<script>
import ArticleHeader from "../components/ArticleHeader.vue";
import ArticleContent from "../components/ArticleContent.vue";
import ArticleAuthor from "../components/ArticleAuthor.vue";

export default {
  name: "home",
  components: {
    ArticleHeader,
    ArticleContent,
    ArticleAuthor
  }
};
</script>
