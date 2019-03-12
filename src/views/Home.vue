<template>
  <div class="home">
    <TopicComponent title="Polska poezja marynistyczna"/>
    <SliderComponent/>
    <ArticleComponent />
    <FooterComponent authors="Autorzy" />
  </div>
</template>

<script>
// @ is an alias to /src
import SliderComponent from "../components/Slider.vue";
import TopicComponent from "../components/TopicComponent.vue";
import FooterComponent from "../components/FooterComponent.vue";
import ArticleComponent from "../components/ArticleComponent.vue";

export default {
  name: "home",
  components: {
    SliderComponent,
    TopicComponent,
    ArticleComponent,
    FooterComponent
  }
};
</script>
