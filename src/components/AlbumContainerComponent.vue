<template>
  <div class="row">
    <div v-for="album in albums" :key="album.title" class="vs-col-5n">
      <AlbumComponent :info="album" />
    </div>
  </div>
</template>

<script>
import AlbumComponent from "./AlbumComponent.vue";

export default {
  name: "AlbumContainerComponent",

  props: {
    albums: Array,
  },

  components: {
    AlbumComponent,
  },
};
</script>

<style lang="scss" scoped>
.vs-col-5n {
  width: calc(100% / 5);
}
</style>