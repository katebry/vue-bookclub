<template>
  <h2>{{ bookTitle }}</h2>
  <button @click="toggleRatings">Show Ratings</button>
  <h1 v-if="this.ratingsVisible">10/10</h1>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Book",
  props: {
    bookTitle: String,
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
