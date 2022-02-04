<template>
  <v-carousel
    cycle
    height="450"
    hide-delimiter-background
    show-arrows-on-hover
    class="mt-10"
  >
    <v-carousel-item
      v-for="(article, i) in slides"
      :key="i"
    > 
      <v-sheet
        :color="colors[1]"
        height="100%"
        v-if="article.slider"
      >
        <v-row
          class="fill-height"
          align="center"
          justify="center"
        >
          <div class="text-h4">
            {{ article.name }}
          </div>
        </v-row>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>
</template>

<script>
  import news from '../assets/articles.json';
  const slides = news.filter(item => item.slider === true);

  const colors = [
          'blue',
          'blue',
        ];
  
  export default {
    data () {
      return {
        slides,
        colors,
      }
    },
  }
</script>