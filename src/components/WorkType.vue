<template>
  <div>
    <div class="type-of-work">
      <p>{{ text }}</p>
    </div>
    <div class="projects" v-for="project in projects" :key="project.name">
      <ProjectCard
        :text="project.name"
        :size="project.size"
        :img="project.img"
      />
    </div>
  </div>
</template>

<script>
import ProjectCard from './ProjectCard'
export default {
  name: 'WorkType',
  components: { ProjectCard },
  props: {
    text: {
      default: 'Other works'
    },
    projects: {
      default: 'Coming soon...'
    }
  }
}
</script>

<style lang="scss">
.type-of-work {
  margin: 10px 0px;
  padding: 10px;
  background-color: lightblue;
  text-align: center;
}


</style>
