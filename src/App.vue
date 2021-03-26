<template>
  <v-app>
    <v-main class="container mt-10">
      <h1 class="text-center pink--text mb-4">Recipe Assistant</h1>
      <v-container>
        <v-row class="justify-center mt-10">
          <v-btn color="pink lighten-3" @click="getRandomRecipes"
            >Find recipes</v-btn>
        </v-row>
        <recipe-results />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import { mapActions } from "vuex";
import RecipeResults from "./components/RecipeResults.vue";
export default {
  components: {
    RecipeResults,
  },
  methods: {
    ...mapActions(["getRandomRecipes"]),
  },
};
</script>
