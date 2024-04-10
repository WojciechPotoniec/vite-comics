<template>
  <HeaderComponent />
  <MainComponent />
  <FooterTopComponent />
  <FooterMidComponent />
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import FooterTopComponent from './components/FooterTopComponent.vue';
import FooterMidComponent from './components/FooterMidComponent.vue';
  export default {
    name: 'App',
    components: {
      HeaderComponent,
      MainComponent,
      FooterTopComponent,
      FooterMidComponent,
    },
    data() {
      return {

      }
    }
  }
</script>

<style lang="scss" scoped>
</style>
