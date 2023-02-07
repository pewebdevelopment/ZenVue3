<template>
    <div>
      <Greet name="Vishvas" heroName="Batman"/>
      <Greet name="Diana" heroName="Superman"/>
      <Article id="my-article" title="Article Title" :likes="50" :isPublished="true" />
    </div>
  </template>
  
  <script>
  import Greet from "../components/10-Components-and-props/Greet.vue";
  import Article from "../components/10-Components-and-props/Article.vue";
export default {
  name:'10-Components-and-props',
  components: {
    Greet,
    Article,
    }
  };
  </script>
  
  <style scoped></style>
  