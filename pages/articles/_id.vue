<template>
  <b-container>
    <div style="margin:30px;" v-html="markdown"></div>
  </b-container>
</template>
 
<script>
//import hello from "../content/articles.md";
export default {
  async asyncData({ params }) {
    const file = await import(`../../content/articles/${params.id}.md`);
    //console.log(params.id);
    return { markdown: file.default };
  }
};
</script> 
<style>
blockquote {
  padding: 11px 20px;
  font-size: 1.25rem;
  background-color: rgba(240, 240, 241, 0.5);
  border-left: 3px solid #c5c6c8;
}
h5 {
  text-align: center;
}
table {
  width: 100%;
  margin: 10px 0;
}
thead > tr {
  background: #ff0000;
  color: #ffffff;
}
tr:nth-child(even) {
  background-color: rgba(0, 0, 0, 0.05);
}
td,
th {
  padding: 10px;
}
</style>