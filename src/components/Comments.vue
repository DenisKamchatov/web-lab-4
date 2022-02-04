<template>
<div class="comments">
  <p class="text-h3 text-center">Comments:</p>
    <v-container>
      <v-row
        v-for="(comment, i) in comments" :key="i"
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
                  <p><span>{{comment.id}}</span> {{comment.name}}</p>
                  <p>{{comment.comment}}</p>
            </div>
          </v-card>
        </v-col>
      </v-row>
      <v-container justify="center">
        <v-row align="center"
      justify="center">
      <form class="comment-form text-center">
        <v-text-field
          v-model="name"
          label="Name"
          required
        ></v-text-field>
        <v-text-field
          v-model="comment"
          label="Comment"
          required
        ></v-text-field>
        <v-btn
          class="mr-4"
          @click="$emit('submitForm', {name, comment})" 
        >
          add comment
        </v-btn>
      </form>
        </v-row>
      </v-container>
    </v-container>
</div>
</template>

<script>
import comments from "../assets/comments.json";
export default {
  name: "Comments",
  data() {
    return {
      comments,
      comment: '',
      name: ''
    };
  }
};
</script>

<style scoped>
.comments {
  margin-top: 30px;
}

.comment-form {
  max-width: 500px;
  margin-top: 30px;
}
</style>