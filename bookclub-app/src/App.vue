<template>
  <Title msg="Book Club" />
  <Book v-for="book in books" :key="book.title" :title="book.title" :rating="book.rating" />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Title from "./components/Title.vue";
import Book from "./components/Book.vue";

export default defineComponent({
  name: "App",
  components: {
    Title,
    Book,
  },
  data: function () {
    return {
      books: [
        {
          title: "Nevada",
          rating: "4.5",
        },
        { title: "One Day in the Life of Ivan Denisovich", rating: "7.4" },
        { title: "Stonefish", rating: "3.9" },
        { title: "The Haunting of Hill House", rating: "8.4" },
      ],
    };
  },
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
