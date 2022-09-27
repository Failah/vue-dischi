<template>
  <div class="card column text-center">
    <img :src="info.poster" :alt="info.title" />
    <p class="text-white">{{ info.title }}</p>
  </div>
</template>

<script>
export default {
  name: "AlbumComponent",

  props: {
    info: Object,
  },
};
</script>

<style lang="scss" scoped>
.card {
  background-color: #2e3a46;
  color: white;
  height: 100%;

  p {
    text-transform: uppercase;
  }
}
</style>