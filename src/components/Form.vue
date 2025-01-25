<template>
    <form>
        <h4 class="text-xl font-semibold mt-6">Add new movie</h4>
        <input type="text" placeholder="Movie title" v-model="newMovieTitle" class="border rounded-md p-1 mt-3" />
        <input type="url" placeholder="Movie url" v-model="newMovieURL" class="border rounded-md p-1 mt-1"/>
        <input type="text" placeholder="Movie year" v-model="newMovieYear" class="border rounded-md p-1 mt-1"/>
        <button class="btn btn-primary" @click.prevent="addMovie">
          Add movie
        </button>
      </form>
</template>

<script>
export default {
    name: "Form",
    data() {
        return {
            newMovieTitle: "",
            newMovieURL: "",
            newMovieYear: 0,
        }
    },
    methods: {
        addMovie() {
        console.log(this.newMovieTitle, this.newMovieURL, this.newMovieYear);
        this.$emit("newProjectEvent", {
            title: this.newMovieTitle,
            img: this.newMovieURL,
            year: this.newMovieYear,
        });

        //this.$emits("nombreDeEvento", datosAPasarAlPadre)
    },
    }
}


</script>

<style></style>