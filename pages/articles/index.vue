<template>
  <b-container>
    <div class="article-container">
      <h1>Articles</h1>
      <b-card v-for="article in data" :key="article.route" v-bind:title="article.title">
        <b-card-text>{{article.description}}</b-card-text>
        <b-button v-bind:href="article.route">Read</b-button>
      </b-card>
    </div>
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

<style lang="scss">
.article-container {
  margin: 30px 0px;
}
</style>