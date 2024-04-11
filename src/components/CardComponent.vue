<template>
  <div>
    <div class="wp-card-img">
        <img :src="image" class="card-img-top" :alt="text" />
    </div>
    <div class="card-body">
      <h5 class="card-text">{{title}}</h5>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardComponent",
  props: ["image", "title", "text"],
};
</script>

<style lang="scss" scoped>
h5{
    text-transform: uppercase;
    color: white;
    font-size: medium;
    margin-top: 20px;
}
.wp-card-img{
    width: 200px;
    height: 200px;
    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
    }
}
</style>
