<template>
  <v-app>
    <v-main class="container mt-10">
          <v-app-bar app color="green darken-3" dark> Recipe Assistant </v-app-bar>
      <v-container>
        <v-row>
          <v-col>
            <key-ingredients />
          </v-col>
          <v-col cols="12" md="4">
            <diet-select />
          </v-col>
          <v-col cols="12" md="4">
            <meal-type-select />
          </v-col>
        </v-row>
        <v-row class="justify-center mt-10">
          <v-btn color="green darken-3"  dark @click="getRandomRecipes"
            >Find recipes</v-btn
          >
        </v-row>
        <recipe-results />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import { mapActions } from "vuex";
import KeyIngredients from "./components/KeyIngredients.vue";
import RecipeResults from "./components/RecipeResults.vue";
import DietSelect from "./components/DietSelect.vue";
import MealTypeSelect from "./components/MealTypeSelect.vue";
export default {
  components: {
    RecipeResults,
    KeyIngredients,
    DietSelect,
    MealTypeSelect,
  },
  methods: {
    ...mapActions(["getRandomRecipes"]),
  },
};
</script>
