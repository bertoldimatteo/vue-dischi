<template>
  <div id="app">
    <BaseHead/>
    <BaseMain/>
  </div>
</template>

<script>
import BaseHead from './components/sections/BaseHead.vue'
import BaseMain from './components/sections/BaseMain.vue'

export default {
  name: 'App',
  components: {
    BaseHead,
    BaseMain
  }
}
</script>

<style lang="scss">
@import 'assets/style/global.scss';
</style>
