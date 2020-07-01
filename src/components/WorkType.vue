<template>
  <div>
    <div class="type-of-work">
      <p>{{ text }}</p>
    </div>
    <div class="projects">
      <ProjectCard
        v-for="project in projects"
        :key="project.name"
        :text="project.name"
        :size="project.size"
        :img="project.img"
      />
    </div>
    <div v-if="text === 'Coder'" class="skills">
      <Skills />
    </div>
  </div>
</template>

<script>
import ProjectCard from './ProjectCard'
import Skills from './Skills'
export default {
  name: 'WorkType',
  components: { ProjectCard, Skills },
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
  margin: 1px 0px;
  padding: 10px;
  // background-color: rgb(226, 230, 173);
  text-align: center;
}

.projects {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;

  .half {
    display: flex;
    width: 49.85vw;
    margin: 1px 0px;
    justify-content: center;
    img,
    .skills {
      width: 49.85vw;
      margin: 1px 0px;
    }
    // .Tetris {
    //   width: 350px;
    //   height: 350px;
    // }

    .skills {
      text-align: center;
      margin-left: 6px;
    }
  }
  .full img {
    margin-top: 3px;
    width: 100vw;
  }
}
</style>
