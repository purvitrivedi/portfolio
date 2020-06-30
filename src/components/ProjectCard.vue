<template>
  <div :class="['card-wrapper', size]">{{ text }}</div>
</template>

<script>
export default {
  name: 'ProjectCard',
  props: ['size', 'text']
}
</script>

<style lang="scss">
.half {
  display: inline-block;
  background-color: red;
  width: 40%;
  margin: 10px;
  padding: 10px;
}

.full {
  background-color: blue;
  margin: 10px;
  padding: 10px;
  color: white;
}
</style>
