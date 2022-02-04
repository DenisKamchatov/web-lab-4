<template>
  <main class="text-center">
    <h1 class="text-h2 name">«{{news[id-1].name}}»</h1>
        <v-img
            :src="require('./../assets/images/' + news[id-1].full_image)"
        ></v-img>
    <div class='text-h5 ma-15 desc'>
        {{news[id-1].desc}}
    </div>
    <div class='text-h6 date'>
       Publication date: {{news[id-1].date}}
    </div>
  </main>
</template>

<script>

import news from '@/assets/articles.json'
export default {
  name: 'Article',
  props: ['id'],
  data(){
      return {
        news
    };
  }
}
</script>

<style scoped>
</style>