<template>
  <h2>{{ bookTitle }}</h2>
  <button @click="toggleRatings">
    {{ ratingsVisible ? "Hide Average Rating" : "Show Average Rating" }}
  </button>
  <h1 v-if="this.ratingsVisible">{{ bookRating }}</h1>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Book",
  props: ["title", "rating"],
  data: function () {
    return {
      bookTitle: this.title,
      bookRating: this.rating,
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
