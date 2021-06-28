<template>
  <h2>{{ title }}</h2>
  <button @click="toggleRatings">
    {{ ratingsVisible ? "Hide Average Rating" : "Show Average Rating" }}
  </button>
  <h1 v-if="this.ratingsVisible">{{ rating }}</h1>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Book",
  props: ["title", "rating"],
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
