<template>
  <div class="home">
    <div class="bio-wrapper">
      <p>
        Software Engineer with experience in User Research.
      </p>
      <p>
        Loves creating music, art & interactive experiences on the web.
      </p>
    </div>
    <div class="work">
      <div class="full"></div>
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
    color: #17224d;
  }

  @media (max-width: 500px) {
    margin: 2em 2em 3.1em 2em;

    p {
      font-size: 1.2em;
    }
  }
}
</style>
