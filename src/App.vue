<template>
  <HeaderComponent />
  <MainComponent />
  <FooterTopComponent />
  <FooterMidComponent />
  <FooterBottomComponent />
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import FooterTopComponent from './components/FooterTopComponent.vue';
import FooterMidComponent from './components/FooterMidComponent.vue';
import FooterBottomComponent from './components/FooterBottomComponent.vue';
  export default {
    name: 'App',
    components: {
      HeaderComponent,
      MainComponent,
      FooterTopComponent,
      FooterMidComponent,
      FooterBottomComponent,
    },
    data() {
      return {

      }
    }
  }
</script>

<style lang="scss" scoped>
</style>
