<template>
  <div>
    
    <HeaderComp />

    <JumboComp />

    <MainComp />

    <FooterComp />

  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue';
import JumboComp from './components/JumboComp.vue';
import MainComp from './components/MainComp.vue';
import FooterComp from './components/FooterComp.vue';


export default {
  name: 'App',
  components: {
    HeaderComp,
    JumboComp,
    MainComp,
    FooterComp
  }
}
</script>

<style lang="scss">
@import './assets/style/general';
@import './assets/style/utilities';
@import './assets/style/vars';
</style>
