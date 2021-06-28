<template>
  <Title msg="Book Club" />
  <Book title="Nevada" rating="4.5/10" />
  <Book title="One Day in the Life of Ivan Denisovich" rating="7.4/10" />
  <Book title="Stonefish" rating="3.9/10" />
  <Book title="The Haunting of Hill House" rating="8.4/10" />
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
