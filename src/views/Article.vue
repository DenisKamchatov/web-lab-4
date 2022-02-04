<template>
  <div >
    <Article v-bind:id="$route.params.id" />
    <Comments @submitForm="submit"/>
  </div>
</template>

<script>
import Article from "@/components/Article.vue";
import Comments from "@/components/Comments.vue";

import comments from "../assets/comments.json";

export default {
  name: "Home",
  components: {
    Article,
    Comments
  },
  methods: {
    submit(data) {
      const lastId = comments[comments.length - 1].id;
      comments.push({id: lastId + 1, name: data.name, comment: data.comment})
    }
  }
};
</script>

<style>
</style>