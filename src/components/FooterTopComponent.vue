<template>
  <footer class="top">
    <div class="container">
      <ul>
        <li v-for="(Card, index) in listCards" :key="index">
          <img :src="Card.img" :alt="Card.title" />
          <a href="#">{{ Card.title }}</a>
        </li>
      </ul>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterTopComponent",
  data() {
    return {
      listCards: [
        {
          img: "../public/img/buy-comics-digital-comics.png",
          title: "Digital Comics",
        },
        {
          img: "../public/img/buy-comics-merchandise.png",
          title: "DC Merchandise",
        },
        {
          img: "../public/img/buy-comics-subscriptions.png",
          title: "Subscription",
        },
        {
          img: "../public/img/buy-comics-shop-locator.png",
          title: "Comic Shop Locator",
        },
        {
          img: "../public/img/buy-dc-power-visa.svg",
          title: "DC Power Visa",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@use "./src/assets/styles/partials/variables" as *;
.top {
  background-color: $bg-color-footer-top;
  padding: 35px 0;
}
img {
  width: 50px;
  height: 60px;
}
ul {
  list-style: none;
  @include wp-flex;
  li {
    margin: 0 20px;
    a {
      color: white;
      text-decoration: none;
      margin: 0 15px;
      text-transform: uppercase;
    }
  }
}
</style>
