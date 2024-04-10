<template>
  <footer class="mid">
    <div class="container d-flex">
      <div class="left">
        <ul class="text-light" v-for="(title, index) in titles" :key="index">
          {{
            title
          }}
          <li v-for="(item, index) in subtitles" :key="index">
            {{ subtitles[index] }}
          </li>
        </ul>
      </div>
      <div class="right">

      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterMidComponent",
  data() {
    return {
      img: "./public/img/dc-logo-bg.png",
      titles: ["dc comics", "dc", "sites", "shop"],
      subtitles: [
        "Characters",
        "Comics",
        "Movies",
        "TV",
        "Games",
        "Videos",
        "News",
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.mid {
  background-image: url(./public/img/footer-bg.jpg);
}
.left {
  display: flex;
  width: 50%;
  img {
    width: 100%;
  }
}
ul {
  list-style: none;
  text-transform: uppercase;
  li {
    text-transform: lowercase;
  }
}
.right {
  width: 50%;
  background-image: url(./public/img/dc-logo-bg.png);
  background-repeat: no-repeat;
  background-position: center;
}
</style>
