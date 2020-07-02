<template>
  <div>
    <div class="projects">
      <div v-for="project in projects" :key="project.name">
        <div :class="project.size">
          <div class="project-wrapper" :id="heading.toLowerCase().split(' ').join('')">
            <img :src="require(`@/assets/${project.img}`)" />
            <div class="project-details">
              <h2>{{ project.name }}</h2>
              <h4>{{ project.description }}</h4>
              <div class="project-links"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div v-if="heading === 'Code'" class="skills">
      <Skills />
    </div>
  </div>
</template>

<script>
import Skills from './Skills'
export default {
  name: 'ProjectCards',
  components: { Skills },
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
.type-of-work {
  margin: 1px 0px;
  padding: 10px;
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
    height: 100%;
    justify-content: center;

    .project-details {
      height: calc(100% - 6px);
    }
  }

  .full {
    img {
      margin-top: 3px;
      width: 100vw;
    }
  }

  .project-details {
    height: calc(100% - 5px);
  }
}

.project-wrapper {
  position: relative;
  overflow: hidden;

  img {
    width: 49.85vw;
    margin: 1px 0px;
  }

  .project-details {
    position: absolute;
    z-index: 100;
    opacity: 0;
    top: 0;
    transition: all 1s ease;
    width: 100%;

    background-color: #1b1b1b;
    color: white;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
}

.project-wrapper:hover {
  .project-details {
    top: 0;
    opacity: 1;
  }
}
</style>
