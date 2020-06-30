<template>
  <div :class="['card-wrapper', size]">
    <img :src="require(`@/assets/${img}`)">
  </div>
</template>

<script>
export default {
  name: 'ProjectCard',
  props: ['size', 'text', 'img']
}
</script>

<style lang="scss">
.half {
  background-color: lightblue;
}

.full {
  width: 100%;
  background-color: rgb(255, 23, 100);
}
</style>
