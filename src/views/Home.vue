<template>
  <div class="home">
    <div class="work">
      <ProjectCards
        v-for="type in work.types"
        :key="type.id"
        :heading="type.heading"
        :projects="type.projects"
      />
    </div>
  </div>
</template>

<script>
import ProjectCards from '../components/ProjectCards'
import types from '../data'

export default {
  name: 'Home',
  components: {
    ProjectCards
  },
  data() {
    return {
      work: { types }
    }
  }
}
</script>
