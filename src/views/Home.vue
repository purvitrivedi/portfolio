<template>
  <div class="home">
    <Bio />
    <div class="work">
      <WorkType
        v-for="type in work.types"
        :key="type.id"
        :text="type.heading"
        :projects="type.projects"
      />
    </div>
  </div>
</template>

<script>
import Bio from '../components/Bio'
import WorkType from '../components/WorkType'

export default {
  name: 'Home',
  components: {
    Bio,
    WorkType
  },
  data() {
    return {
      work: {
        types: [
          {
            id: 1,
            heading: 'Coder',
            projects: [
              {
                name: 'Search & Play',
                size: 'half',
                img: 'logo.png'
              },
              {
                name: 'Tetris',
                size: 'half',
                img: 'logo.png'
                
              },
              {
                name: 'Filtr',
                size: 'full',
                img: 'logo.png'
              },
              {
                name: 'Hikr',
                size: 'full',
                img: 'logo.png'
              }
            ]
          },
          {
            id: 2,
            heading: 'User Researcher',
            projects: [
              {
                name: 'LUMI',
                size: 'half',
                img: 'logo.png'
              },
              {
                name: 'ROLI Studio Player',
                size: 'half',
                img: 'logo.png'
              }
            ]
          },
          {
            id: 3,
            heading: 'Music projects',
            projects: [
              {
                name: 'KALA',
                size: 'half',
                img: '../assets/logo.png'
              },
              {
                name: 'Women in Music Tech',
                size: 'half',
                img: '../assets/logo.png'
              }
            ]
          }
        ]
      }
    }
  }
}
</script>
