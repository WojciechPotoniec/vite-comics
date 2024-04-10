<template>
  <header class="container">
    <nav class="d-flex justify-content-between align-items-center py-3">
      <img :src="img" alt="DC logo" />
      <ul class="d-flex">
        <li v-for="(item, index) in navlist" :key="index">
          <a href="#">{{ item }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",
  data() {
    return {
      img: "../public/img/dc-logo.png",
      navlist: [
        "Characters",
        "Comics",
        "Movies",
        "TV",
        "Games",
        "Collectibles",
        "Videos",
        "Fans",
        "News",
        "Shop",
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@use "./src/assets/styles/partials/variables" as *;
header {
  background-color: $bg-color-header;
}
ul {
  list-style: none;
  li {
    margin: 0 15px;
    a {
      text-decoration: none;
      color: black;
      text-transform: uppercase;
      &:hover {
        border-bottom: $bg-color-footer-top solid 5px;
      }
    }
  }
}
</style>
