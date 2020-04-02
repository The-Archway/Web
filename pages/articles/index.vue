<template>
  <b-container>
    <h1>Articles</h1>
    <b-card v-for="article in data" :key="article.route" v-bind:title="article.title">
      <b-card-text>{{article.description}}</b-card-text>
      <a v-bind:href="article.route">Read</a>
    </b-card>
  </b-container>
</template>

<script>
import articles from "../../content/articles.json";

export default {
  data() {
    return {
      data: articles
    };
  },
  async asyncData() {}
};
</script>

<style lang="scss" scoped>
</style>