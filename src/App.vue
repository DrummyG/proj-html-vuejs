<template>
  <div id="app">
    <app-head />

    <app-main />

    <app-footer />
  </div>
</template>

<script>
import AppHead from './components/AppHead.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  name: 'App',
  components: {
    AppHead,
    AppMain,
    AppFooter
  }
}
</script>

<style lang="scss">
@import './assets/styles/generals.scss';
@import './assets/styles/variables.scss';
#app {

}
</style>
