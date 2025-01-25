<template>

    <div class="grid">
    <div v-for="mv in movies">
      <!-- un card de una pelicula -->
      <Card :movie="mv"></Card>
    </div>
    
  </div>

</template>

<script>
import Card from "./Card.vue"

export default {
    name: "MoviesGrid",
    components: { Card},
    props: ["movies"]
}
</script>

<style>

.grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: 300px;
  gap: 80px 30px;
  padding-bottom: 50px;
  padding-top: 50px;
}</style>