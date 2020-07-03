<template>
  <div id="app">
    <Header />
    <router-view />
    <Contact />
  </div>
</template>

<script>
import Header from './components/layout/Header'
import Contact from './components/layout/Contact'

export default {
  name: 'app',
  components: {
    Header,
    Contact
  }
}
</script>

<style lang="scss">
body {
  margin: 0px;
  // font-family: 'Questrial', sans-serif;
  font-family: 'Montserrat', sans-serif;
  background-color: #ebebeb;
}
</style>
