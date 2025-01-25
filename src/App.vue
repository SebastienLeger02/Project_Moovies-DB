<template>
  <main>
    <div class="container">
      <h1>My Movies Database</h1>
      <!-- GRID DE PELICULAS -->
      <MoviesGrid :movies="movies"></MoviesGrid>

      <!-- FORMULARIO -->
      <Form @newProjectEvent="receiveProject"/>

    </div>
  </main>
</template>

<script>
import MoviesDB from "./Movies.js";
import MoviesGrid from "./components/MoviesGrid.vue";
import Form from "./components/Form.vue"
export default {
  name: "App",
  components: {
    MoviesGrid,
    Form
  },
  data() {
    return {
      movies: MoviesDB, //el array de todas las peliculas
    };
  },
  methods: {
    receiveProject(info) {
      this.movies.push(info)
    }
  },
};
</script>

<style>

body {
  background: rgb(238,237,174);
  background: radial-gradient(circle, rgba(238,237,174,1) 0%, rgba(211,109,25,1) 100%);
}

.container {
  max-width: 1000px;
  margin: 20px auto;
  text-align: center;
}
h1 {
  color: #803100;
  font-size: 60px;
  padding-bottom: 30px;
  font-weight: 600;
  font-family: "Acme", serif;
  font-style: normal;
}

button {
  margin: 10px;
}

form {
  display: flex;
  flex-direction: column;
  width: 400px;
  margin: 0 auto;
  padding-top: 100px; 
}

</style>
