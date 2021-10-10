<template>
  <div>
    <label>
      Name
      <input type="text" v-model="newMovieName" />
    </label>
    <label>
      Data
      <input type="text" v-model="newMovieData" />
    </label>
    <button @click="onCreateMovieHandle">Create</button>
  </div>
</template>

<script>
export default {
  name: "CreateMovieForm",
  data() {
    return {
      newMovieName: "",
      newMovieData: "",
    };
  },
  methods: {
    onCreateMovieHandle() {
      this.$emit("create", this.newMovieName, this.newMovieData);
    },
  },
};
</script>

<style lang="scss" scoped></style>
