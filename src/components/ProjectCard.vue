<template>
  <div :class="size">
    <img :src="require(`@/assets/${img}`)" :class="text" />
  </div>
</template>

<script>
export default {
  name: 'ProjectCard',
  props: ['size', 'text', 'img']
}
</script>

<style lang="scss">
</style>
