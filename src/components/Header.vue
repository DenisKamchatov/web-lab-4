<template>
  <v-container>
    <v-toolbar flat class="mainHeader">
      <v-toolbar-title>
        <router-link to="/">ЛОГО</router-link>
        </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-text-field
        hide-details
        prepend-icon="mdi-magnify"
        single-line
      ></v-text-field>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-xs-only">
        <v-btn><router-link to="/">Главная</router-link></v-btn>
        <v-btn><router-link to="/news">Новости</router-link></v-btn>
        <v-btn><router-link to="/gallery">Галерея</router-link></v-btn>
      </v-toolbar-items>
      <div class="hidden-sm-and-up">
        <v-menu offset-y>
          <template v-slot:activator="{ on }">
            <v-app-bar-nav-icon v-on="on"></v-app-bar-nav-icon>
          </template>
          <v-list class="responsiveMenu">
            <v-list-item>
              <v-list-item-title><router-link to="/">Главная</router-link></v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title><router-link to="/news">Новости</router-link></v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title><router-link to="/gallery">Галерея</router-link></v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
      </div>
    </v-toolbar>
  </v-container>
</template>

<script>
  
  export default {
    data () {
      return {
      }
    },
  }
</script>