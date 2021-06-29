<template>
    <p>Kate: {{ scores.kate }}</p>
    <p>Neal: {{ scores.neal }}</p>
    <p>GG: {{ scores.gg }}</p>
    <p>Clinch: {{ scores.clinch }}</p>
    <p>Tim: {{ scores.tim }}</p>
    <p>Charlotte: {{ scores.charlotte }}</p>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Ratings",
  props: {
    scores: {
      type: Object,
      required: true,
    },
  },
});
</script>


