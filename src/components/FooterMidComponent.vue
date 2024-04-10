<template>
  <footer class="mid">
    <div class="container">
      <div class="left">
        <ul>
            <li>
                
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
    return {};
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
  width: 50%;
  img {
    width: 100%;
  }
}
</style>
