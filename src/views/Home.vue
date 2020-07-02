<template>
  <div class="home">
    <Bio />
    <div class="work">
      <div class="types">
        <a v-for="type in types" :key="type" :href="`#${type.toLowerCase().split(' ').join('')}`">{{ type }}</a>
      </div>
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
import Bio from '../components/Bio'
import ProjectCards from '../components/ProjectCards'

export default {
  name: 'Home',
  components: {
    Bio,
    ProjectCards
  },
  data() {
    return {
      types: ['Code', 'User Research', 'Music'],

      work: {
        types: [
          {
            id: 1,
            heading: 'Code',
            projects: [
              {
                name: 'Filtr',
                description:
                  'Image-editing app using Python, Django, PostgreSQL & React.js.',
                size: 'half',
                img: 'filtr.png'
              },
              {
                name: 'Tetris',
                description: 'Vanilla JavaScript, HTML & CSS.',
                size: 'half',
                img: 'tetris-5.png'
              },
              {
                name: 'Hikr',
                description:
                  'A full-stack Hike search & community app made using Node.js, Express, MongoDB & React.js',
                size: 'full',
                img: 'hikr-2.png'
              },

              {
                name: 'Search & Play',
                description:
                  'An interactive music search & play app made using React.js and iTunes Search API',
                size: 'full',
                img: 'search-play.png'
              }
            ]
          },
          {
            id: 2,
            heading: 'User Research',
            projects: [
              {
                name: 'LUMI',
                size: 'half',
                img: 'tetris-5.png'
              },
              {
                name: 'ROLI Studio Player',
                size: 'half',
                img: 'tetris-5.png'
              }
            ]
          },
          {
            id: 3,
            heading: 'Music',
            projects: [
              {
                name: 'KALA',
                size: 'half',
                img: 'tetris-5.png'
              },
              {
                name: 'Women in Music Tech',
                size: 'half',
                img: 'tetris-5.png'
              }
            ]
          }
        ]
      }
    }
  }
}
</script>

<style lang="scss">
.types {
  display: flex;
  justify-content: center;

  a {
    margin: 15px;
    color: black;
  }
}
</style>
