<template>
  <div class="card column text-center p-3">
    <img class="img-fluid" :src="info.poster" :alt="info.title" />
    <p class="h4 text-white my-3">{{ info.title }}</p>
    <span>{{ info.author }}</span>
    <span>{{ info.year }}</span>
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

  span {
    color: #64676b;
  }
}
</style>