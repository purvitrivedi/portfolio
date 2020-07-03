<template>
  <div class="about">
    <Bio />
    <Skills />
  </div>
</template>

<script>
import Skills from '../components/Skills'
import Bio from '../components/Bio'
export default {
  components: { Skills, Bio }
}
</script>

<style lang="scss">
.about {
  height: 85vh;
  display: flex;


}
</style>
