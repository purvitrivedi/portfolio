<template>
  <div class="type-of-work">
    {{ text }}
  </div>
</template>

<script>
export default {
  name: 'WorkType',
  props: {
    text: {
      type: String,
      required: false,
      default: 'Other works',
      validator: string => string.length > 0
    }
  }
}
</script>
