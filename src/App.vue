<template>
  <v-app>

  <v-app-bar app>
    <Header />
  </v-app-bar>

  <v-main>
    <v-container fluid>
      <router-view></router-view>
    </v-container>
  </v-main>

  <v-footer app>
    <!-- -->
  </v-footer>
</v-app>
</template>

<script>
import Header from '@/components/Header.vue';

export default {
  name: 'App',

  components: {
    Header
  },

  data: () => ({
    //
  }),
};
</script>
