<template>
  <header>
    <img src="../assets/img/logo.png" alt="Spotify Logo" />
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",
};
</script>

<style lang="scss" scoped>
header {
  height: 80px;
  background-color: #2e3a46;
  padding: 10px;

  img {
    height: 60px;
  }
}
</style>