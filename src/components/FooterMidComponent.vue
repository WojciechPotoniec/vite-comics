<template>
  <footer class="mid">
    <div class="container d-flex">
      <div class="left">
        <ul class="text-light" v-for="(mainlist, index) in mainlists" :key="index">
          <h4>
            {{mainlist.title}}
          </h4>
          <li v-for="(item, i) in mainlist.list" :key="i">
            <a href="#">{{ item }}</a>
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
      mainlists: [
                    {
                        title: 'DC COMICS',
                        list: [
                          'Characters',
                            'Comics',
                            'Movies',
                            'TV',
                            'Games',
                            'Videos',
                            'News'
                        ]
                    },
                    {
                        title: 'DC',
                        list: [
                            'Terms Of Use',
                            'Privacy policy (New)',
                            'Ad Choices',
                            'Advertising',
                            'Jobs',
                            'Subscriptions',
                            'Talent Workshops',
                            'CPSC Certificates',
                            'Ratings',
                            'Shop Help',
                            'Contact Us'
                        ]
                    },
                    {
                        title: 'SITES',
                        list: [
                            'DC',
                            'MAD Magazine',
                            'DC Kids',
                            'DC Universe',
                            'DC Power Visa'
                        ]
                    },
                    {
                        title: 'SHOP',
                        list: [
                            'Shop DC',
                            'Shop DC Collectibles'
                        ]
                    }
                ],
    };
  },
};
</script>

<style lang="scss" scoped>
@use "./src/assets/styles/partials/variables" as *;
.mid {
  background-image: url(./public/img/footer-bg.jpg);
  background-repeat: no-repeat;
  background-size: cover;
}
.left {
  display: flex;
  flex-wrap: wrap;
  width: 40%;
}
ul{
  list-style: none;
  margin-top: 30px;
}
span{
  text-transform: uppercase;
  font-weight: 900;
}
a{
  text-decoration: none;
  color: grey;
  font-size: 0.9rem;
  &:hover{
    color: $bg-color-footer-top;
  }
}

.right {
  width: 60%;
  background-image: url(./public/img/dc-logo-bg.png);
  background-repeat: no-repeat;
  background-position: center;
}
</style>
