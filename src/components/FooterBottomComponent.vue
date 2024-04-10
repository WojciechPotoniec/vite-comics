<template>
  <footer class="bottom">
    <div class="container d-flex justify-content-between align-items-center py-4">
      <div>
        <button class="text-uppercase">sign-up now!</button>
      </div>
      <div>
        <ul class="d-flex align-items-center">
          <span>Follow Us</span>
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
button{
  border: $bg-color-footer-top solid 2px;
  padding: 6px;
  background-color: transparent;
  color: white;
}
ul {
  list-style: none;
  span {
    color: $bg-color-footer-top;
    text-transform: uppercase;
  }
  a {
    text-decoration: none;
    margin-left: 20px;
  }
}
</style>
