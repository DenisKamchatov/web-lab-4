<template>
  <div class="text-center">
    <h1>Новости</h1>
    <div>
    <v-container
      class="grey lighten-5 mb-6"
      fluid
    >
      <v-row
        v-for="(article, i) in news" :key="i"
        align="start"
        no-gutters
        class="ma-20"
      >
        <v-col
        >
          <v-card
            class="pa-2"
            outlined
            tile
          >
            <div class="text-h5 pa-2">
                <router-link :to="'/article/' + article.id">
                <v-img
                  max-height="300"
                  :src="require('./../assets/images/' + article.preview_image)"
                ></v-img>
                  {{article.shortDesc}}
                </router-link>
            </div>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
  </div>
</template>

<script>
import news from "../assets/articles.json";

export default {
  name: "News",
  data() {
    return {
      news,
    };
  }
};
</script>