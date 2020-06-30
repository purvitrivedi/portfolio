<template>
  <div class="home">
    <Bio />
    <WorkType text="Coder" />
    <hr />
    <ProjectCard size="half" text="card 1" />
    <ProjectCard size="half" text="card 2" />
    <ProjectCard size="full" text="card 3" />
    <ProjectCard size="full" text="card 4" />
    <WorkType text="User Researcher" />
    <hr />
  </div>
</template>

<script>
import Bio from '../components/Bio'
import WorkType from '../components/WorkType'
import ProjectCard from '../components/ProjectCard'
export default {
  name: 'Home',
  components: {
    Bio,
    WorkType,
    ProjectCard
  }
}
</script>
