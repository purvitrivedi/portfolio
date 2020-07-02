<template>
  <div>
    <div class="projects">
      <div v-for="project in projects" :key="project.name">
        <div :class="project.size">
          <div
            class="project-wrapper"
            :id="
              heading
                .toLowerCase()
                .split(' ')
                .join('')
            "
          >
            <img :src="require(`@/assets/${project.img}`)" />
            <div class="project-details">
              <h2>{{ project.name }}</h2>
              <h4>{{ project.description }}</h4>
              <div class="project-links">
                <a :href="project.website" target="_blank"
                  ><i class="fas fa-link"></i
                ></a>
                <a
                  v-if="heading === 'Code'"
                  :href="project.source"
                  target="_blank"
                  ><i class="fab fa-github"></i
                ></a>
              </div>
            </div>
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
    transition: all 0.3s ease;
    width: 100%;

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
      font-size: 40px;
      color: white;
    }
  }
}

.project-wrapper:hover {
  .project-details {
    top: 0;
    opacity: 1;
  }
}
</style>
