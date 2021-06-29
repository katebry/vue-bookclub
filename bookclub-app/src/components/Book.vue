<template>
  <h2>{{ title }}</h2>
  <button @click="toggleRatings">
    {{ ratingsVisible ? "Hide Average Rating" : "Show Average Rating" }}
  </button>
  <h1 v-if="this.ratingsVisible">{{ rating }}</h1>
  <p v-if="this.ratingsVisible">
    <Ratings :scores="scores" />
  </p>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Ratings from "./Ratings.vue";

export default defineComponent({
  components: {
    Ratings,
  },
  name: "Book",
  props: {
    title: {
      type: String,
      required: true,
    },
    rating: {
      type: String,
      required: true,
    },
    scores: Object,
  },
  data: function () {
    return {
      ratingsVisible: false,
    };
  },
  methods: {
    toggleRatings() {
      this.ratingsVisible = !this.ratingsVisible;
    },
  },
});
</script>

<style>
button {
  background-color: #42b983;
}
</style>
