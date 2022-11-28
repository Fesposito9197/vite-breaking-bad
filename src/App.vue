<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter
  }
}
</script>

<template>
  <AppHeader/>
  <AppMain/>
  <AppFooter/>
</template>

<style lang="scss">
body{
  background-color: var(--my-primary-color)!important
}
@import './style/global.scss';
</style>
