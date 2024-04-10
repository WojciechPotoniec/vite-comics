<template>
  <footer class="bottom">
    <div class="container d-flex justify-content-between align-items-center py-4">
      <div>
        <button>SIGN-UP NOW!</button>
      </div>
      <div>
        <ul class="d-flex align-items-center">
          <a class="text-uppercase" href="#">Follow Us!</a>
          <li v-for="(item, index) in iconimgs" :key="index">
            <a href="#"><img :src="item.img" :alt="item.title" /></a>
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterBottomComponent",
  data() {
    return {
      iconimgs: [
        {
          img: "./public/img/footer-facebook.png",
          title: "Facebook",
        },
        {
          img: "./public/img/footer-twitter.png",
          title: "Twitter",
        },
        {
          img: "./public/img/footer-youtube.png",
          title: "Youtube",
        },
        {
          img: "./public/img/footer-pinterest.png",
          title: "Pinterest",
        },
        {
          img: "./public/img/footer-periscope.png",
          title: "Periscope",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@use "./src/assets/styles/partials/variables" as *;
.bottom {
  background-color: $bg-color-footer-bottom;
}
ul {
  list-style: none;
}
a {
  text-decoration: none;
  color: $bg-color-footer-top;
  margin-right: 20px;
}
</style>
