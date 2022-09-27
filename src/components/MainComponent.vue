<template>
  <main>
    <div class="container pt-5">
      <AlbumContainerComponent :albums="albums" />
    </div>
  </main>
</template>

<script>
import AlbumContainerComponent from "@/components/AlbumContainerComponent.vue";
import axios from "axios";

export default {
  name: "MainComponent",
  components: {
    AlbumContainerComponent,
  },

  data() {
    return {
      apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
      albums: [],
    };
  },

  created() {
    axios
      .get(this.apiUrl)
      .then((response) => {
        this.albums = response.data.response;
        console.log(response.data.response);
      })
      .catch((error) => {
        console.log(error);
      });
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