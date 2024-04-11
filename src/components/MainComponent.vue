<template>
  <div id="hero"></div>
  <main>
    <div class="container">
      <h3>Current series</h3>
      <div class="row">
        <div
          class="col-12 col-sm-6 col-md-4 col-lg-3 col-xl-2 mb-4"
          v-for="(item, index) in comics"
          :key="index"
        >
          <CardComponent
            :image="item.thumb"
            :title="item.series"
            :text="item.type"
          />
        </div>
      </div>
      <div class="load">
        <button>Load More</button>
      </div>
    </div>
  </main>
</template>

<script>
import { comics } from "../data/data.js";
import CardComponent from "./CardComponent.vue";
export default {
  name: "MainComponent",
  components: {
    CardComponent,
  },
  data() {
    return {
      comics: comics,
    };
  },
};
</script>

<style lang="scss" scoped>
@use "./src/assets/styles/partials/variables" as *;
#hero {
  background-image: url(../public/img/jumbotron.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  height: 400px;
}
main {
  background-color: $bg-color-main;
  padding: 40px 0;
}
h2 {
  margin: 0;
}
h3 {
  background-color: $bg-color-footer-top;
  display: inline-block;
  transform: translate(0, -140%);
  padding: 5px 20px;
  color: white;
  text-transform: uppercase;
}
.load{
    @include wp-flex;
    button{
        background-color: $bg-color-footer-top;
        padding: 6px 50px;
        text-transform: uppercase;
        color: white;
        border: none;
        font-size: small;
        font-weight: 600;
        cursor: pointer;
    }
}
</style>
