<template>
  <div>
    <select
      v-model="inputText"
      @click="$emit('genre-search', inputText)"
      name="genre-filter"
      id="genre-filter"
    >
      <option value="rock">Rock</option>
      <option value="pop">Pop</option>
      <option value="jazz">Jazz</option>
      <option value="metal">Metal</option>
    </select>
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
};
</script>

<style lang="scss" scoped>
</style>