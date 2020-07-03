<template>
  <div class="home">
    <div class="bio-wrapper">
      <p>
        Software Engineer with experience in User Research.
      </p>
      <p>
        Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis
        suscipit laboriosam nisi.
      </p>
    </div>
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

<style lang="scss">
.bio-wrapper {
  margin: 3.3em 2em 4.1em 2em;

  p {
    font-weight: 500;
    margin: 5px;
    font-size: 1.4rem;
  }
}
</style>
