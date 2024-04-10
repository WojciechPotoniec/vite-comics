<template>
  <header class="container">
    <img :src="img" alt="DC logo"/>
    <h2>Header</h2>
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",
  data() {
    return {
        img: "../public/img/dc-logo.png"
    };
  },
};
</script>

<style lang="scss" scoped>
@use "./src/assets/styles/partials/variables" as *;
header {
  background-color: $bg-color-header;
}
</style>
