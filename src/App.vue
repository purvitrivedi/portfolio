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
@font-face {
  font-family: 'Space';
  src: url('./styles/otf/SpaceGrotesk-Regular.otf');

  font-family: 'Space Bold';
  src: url('./styles/otf/SpaceGrotesk-Bold.otf');
}
body {
  margin: 0px;
  // font-family: 'Questrial', sans-serif;
  font-family: 'Montserrat', sans-serif;
  font-family: 'Space', sans-serif;
  background-color: #f0f4ff;
}
</style>
