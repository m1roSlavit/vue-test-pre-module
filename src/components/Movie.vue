<template>
  <div>
    <div>{{ movieData.title }}</div>
    <div>{{ movieData.date }}</div>
    <slot :title="movieData.title"></slot>
  </div>
</template>

<script>
export default {
  name: "Movie",
  props: {
    movieData: {
      type: Object,
      default: () => ({}),
    },
  },
};
</script>

<style lang="scss" scoped></style>
