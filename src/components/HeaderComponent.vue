<template>
  <header class="container">
    <nav class="py-3">
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
nav {
  @include wp-flex;
}
ul {
  list-style: none;
  li {
    margin: 0 15px;
      a {
        text-decoration: none;
        color: black;
        font-weight: 600;
        text-transform: uppercase;
        position: relative;
      }
      a:hover{
        color: $bg-color-footer-top;
      }
      a::after{
        content: "";
        position: absolute;
        left: 0;
        top: 81px;
        width: 100%;
        height: 5px;
        background-color: $bg-color-footer-top;
        visibility: hidden;
      }
      a:hover::after{
        visibility: visible;
      }
    }
  }
</style>
