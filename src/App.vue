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
  @import './styles/general.scss';
</style>
