<template>
  <div>
    <div>
      <movie v-for="(movie, idx) in movies" :key="idx" :movieData="movie">
        <template v-slot="movieProp">
          <strong>{{ movieProp.title.toUpperCase() }}</strong>
        </template>
      </movie>
    </div>
    <create-movie-form @create="createMovie" />
  </div>
</template>

<script>
import CreateMovieForm from "./CreateMovieForm.vue";
import Movie from "./Movie.vue";

export default {
  components: { CreateMovieForm, Movie },
  name: "MovieList",
  data() {
    return {
      movies: [],
    };
  },
  methods: {
    createMovie(title, date) {
      this.movies.push({
        title,
        date,
      });
    },
  },
};
</script>

<style lang="scss" scoped></style>
