<template>
  <div class="row align-items-center pb-3">
    <div class="row col-6 align-items-center">
      <h4 class="col-4">Sort by Genre:</h4>
      <select
        v-model="inputText"
        @click="$emit('genre-search', inputText)"
        name="genre-filter"
        id="genre-filter"
        class="col-6 px-2 h-75"
        value="All"
      >
        <option value="All">All</option>
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>
      </select>
    </div>
    <div class="row col-6"></div>
  </div>
</template>

<script>
export default {
  name: "GenreFilterComponent",

  data() {
    return {
      inputText: "",
    };
  },

  mounted() {
    this.inputText = "All";
  },
};
</script>

<style lang="scss" scoped>
#genre-filter {
  color: rgb(68, 68, 68);
  outline: 0px;
}
</style>