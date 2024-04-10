<template>
  <HeaderComponent />
  <MainComponent />
  <FooterTopComponent />
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import FooterTopComponent from './components/FooterTopComponent.vue';
  export default {
    name: 'App',
    components: {
      HeaderComponent,
      MainComponent,
      FooterTopComponent,
    },
    data() {
      return {

      }
    }
  }
</script>

<style lang="scss" scoped>
</style>
