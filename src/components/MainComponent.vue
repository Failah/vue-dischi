<template>
  <main>
    <div class="container pt-5">
      <GenreFilterComponent @genre-search="searchAlbumByGenre" />
      <AlbumContainerComponent :albums="albums" />
    </div>
  </main>
</template>

<script>
import AlbumContainerComponent from "@/components/AlbumContainerComponent.vue";
import GenreFilterComponent from "@/components/GenreFilterComponent.vue";
import axios from "axios";

export default {
  name: "MainComponent",
  components: {
    AlbumContainerComponent,
    GenreFilterComponent,
  },

  data() {
    return {
      apiAlbumsUrl: "https://flynn.boolean.careers/exercises/api/array/music",
      albums: [],
    };
  },

  created() {
    axios
      .get(this.apiAlbumsUrl)
      .then((response) => {
        this.albums = response.data.response;
        console.log(response.data.response);
      })
      .catch((error) => {
        console.log(error);
      });
  },

  methods: {
    searchAlbumByGenre(searchText) {
      console.log(searchText);
    },
  },
};
</script>

<style lang="scss" scoped>
main {
  background-color: #1e2d3b;
  color: white;
  height: calc(100vh - 80px);
  overflow-y: scroll;
}
</style>