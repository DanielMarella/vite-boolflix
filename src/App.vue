<script>
import HeaderApp from './components/HeaderApp.vue';
import MainApp from './components/MainApp.vue';
export default {
  name : 'App',

  components : {
    HeaderApp,
    MainApp,
  }


}
</script>

<template>
  <div>
    <HeaderApp />
    <MainApp />
  </div>
</template>
<style lang="scss">
  @import '../node_modules/bootstrap/scss/bootstrap';
  @import './styles/general.scss';
</style>
