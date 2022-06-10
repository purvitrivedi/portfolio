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
        <a class="project-details">
          <div class="details-wrap">
            <h2>{{ project.name }}</h2>
            <p class="description">{{ project.description }}</p>
            <div v-if="project.name === 'Filtr'">
              <SkillsFiltr />
            </div>
            <div v-if="project.name === 'Hikr'">
              <SkillsHikr />
            </div>
            <div v-if="project.name === 'Search + Play'">
              <SkillsSP />
            </div>
            <div v-if="project.name === 'Tetris'">
              <SkillsTetris />
            </div>
            <div class="music-links">
              <a
                v-if="heading !== 'Music'"
                :href="project.website"
                target="_blank"
              >
                <i class="fas fa-link"></i>
              </a>
              <a
                v-if="heading === 'Music'"
                :href="project.itunes"
                target="_blank"
              >
                <i class="fab fa-apple"></i>
              </a>
              <a
                v-if="heading === 'Music'"
                :href="project.spotify"
                target="_blank"
              >
                <i class="fab fa-spotify"></i>
              </a>
              <a
                v-if="heading === 'Code'"
                :href="project.source"
                target="_blank"
                ><i class="fab fa-github"></i
              ></a>
            </div>
          </div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import SkillsFiltr from '../components/skills/SkillsFiltr'
import SkillsHikr from '../components/skills/SkillsHikr'
import SkillsSP from '../components/skills/SkillsSP'
import SkillsTetris from '../components/skills/SkillsTetris'
export default {
  name: 'ProjectCards',
  components: { SkillsFiltr, SkillsHikr, SkillsSP, SkillsTetris },
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
  overflow: hidden;

  .half {
    display: flex;
    justify-content: center;
    width: 49.85%;
    height: 50vh;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    margin-bottom: 5px;

    @media (max-width: 500px) {
      width: 100vw;
    }

    .project-details {
      width: 100%;
      height: 50vh;
      @media (max-width: 500px) {
        width: 100vw;
      }
    }
  }

  .full {
    width: 100vw;
    height: 55vh;
    margin-bottom: 5px;

    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;

    @media (max-width: 500px) {
      background-size: auto;
    }
    .project-details {
      width: 100vw;
      height: 55vh;
    }
  }
}

.project-wrapper {
  position: relative;
  width: 100%;

  .project-details {
    opacity: 0;
    transition: all 0.3s ease;

    background-color: #5220dd;
    color: white;

    display: flex;
    flex-direction: column;
    justify-content: center;

    .details-wrap {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      h2 {
        margin: 0px 0px 15px 0px;
      }

      .description {
        margin: 0px 0px 30px 0px;
        padding: 0px 10px;
      }

      @media (max-width: 375px) {
        .description {
          font-size: 14px;
          padding: 0px 20px;
        }
      }
      .project-links,
      .music-links {
        a {
          font-size: 35px;
          color: #ffc647;
          margin: 0px 10px;

          @media (max-width: 350px) {
            margin-top: 5px;
            font-size: 25px;
          }
        }

        a:hover {
          color: white;
        }
      }

      .music-links {
        .fa-apple {
          font-size: 40px;
        }
        display: flex;
        justify-content: center;
        align-items: center;
      }
    }
  }
}

.project-wrapper:hover {
  .project-details {
    opacity: 1;
  }
}
.project-wrapper:active {
  .project-details {
    opacity: 1;
  }
}
</style>
