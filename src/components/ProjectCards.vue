<template>
  <div class="projects">
    <div
      v-for="project in projects"
      :key="project.name"
      :class="project.size"
      v-bind:style="{
        backgroundImage: 'url(' + require(`../assets/${project.img}`) + ')'
      }"
    >
      <div
        class="project-wrapper"
        :id="
          heading
            .toLowerCase()
            .split(' ')
            .join('')
        "
      >
        <div class="project-details">
          <h2>{{ project.name }}</h2>
          <h4>{{ project.description }}</h4>
          <div class="project-links">
            <a :href="project.website" target="_blank"
              ><i class="fas fa-link"></i
            ></a>
            <a v-if="heading === 'Code'" :href="project.source" target="_blank"
              ><i class="fab fa-github"></i
            ></a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProjectCards',
  props: {
    heading: {
      default: 'Other works'
    },
    projects: {
      default: 'Coming soon...'
    }
  }
}
</script>

<style lang="scss">
.projects {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;

  .half {
    display: flex;
    width: 49.85vw;
    justify-content: center;
    height: 50vh;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    margin-bottom: 5px;

    .project-details {
      width: 49.85vw;
      height: 50vh;
    }
  }

  .full {
    width: 100vw;
    height: 55vh;
    margin-bottom: 5px;

    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;

    .project-details {
      width: 100vw;
      height: 55vh;
    }
  }
}

.project-wrapper {
  position: relative;
  overflow: hidden;

  .project-details {
    opacity: 0;
    transition: all 0.3s ease;

    background-color: #1b1b1b;
    color: white;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .project-links {
    a {
      margin: 10px;
      font-size: 30px;
      color: #06d6a0;
    }
  }
}

.project-wrapper:hover {
  .project-details {
    opacity: 1;
  }
}
</style>
