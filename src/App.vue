<template>
  <div id="app">
    <Header />
    <router-view />
  </div>
</template>

<script>
import Header from './components/layout/Header'

export default {
  name: 'app',
  components: {
    Header
  }
}
</script>

<style lang="scss">
body {
  margin: 0px;
  // font-family: 'Questrial', sans-serif;
  font-family: 'Montserrat', sans-serif;
  background-color: #F0F4FF;
}
</style>
