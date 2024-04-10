<template>
  <footer class="mid">
    <div class="container">
      <div class="left">
        <ul class="text-light" v-for="(title, index) in titles" :key="index">
            {{title}}
            <li v-for="(item, index) in subtitles" :key="index">
                {{subtitles[index]}}
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
        titles: [
            "dc comics","dc", "sites", "shop"
        ],
        subtitles:[
            "Characters", "Comics", "Movies", "TV", "Games", "Videos", "News"
        ]
    };
  },
};
</script>

<style lang="scss" scoped>
.mid {
  background-image: url(./public/img/footer-bg.jpg);
}
.right {
  width: 50%;
}
.left {
  background-image: url(./public/img/dc-logo-bg.png);
  background-repeat: no-repeat;
  width: 50%;
  img {
    width: 100%;
  }
}
</style>
