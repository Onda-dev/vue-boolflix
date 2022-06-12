<template>
  <div id="app">
    <HeaderComponent/>
    <MainComponent/>
  </div>
</template>

<script>
import HeaderComponent from './components/blocks/HeaderComponent.vue'
import MainComponent from './components/blocks/MainComponent.vue'


export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent
  }
}
</script>

<style land="scss">
@import 'assets/style/global.scss'

</style>
