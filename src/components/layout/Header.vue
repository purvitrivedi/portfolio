<template>
  <div class="nav">
    <router-link to="/" class="name">PURVI TRIVEDI</router-link>
    <div class="nav-items">
      <router-link
        v-for="type in types"
        :key="type"
        to="/"
        v-scroll-to="
          `#${type
            .toLowerCase()
            .split(' ')
            .join('')}`
        "
        tag="a"
      >
        {{ type }}
      </router-link>
      <div class="about-nav">
        <router-link to="/about" tag="a">contact</router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      types: ['code', 'uxresearch', 'music']
    }
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700;800&display=swap');

.nav {
  margin-top: 1.7em;
  padding: 0px 0.85em;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;

  @media (max-width: 500px) {
    flex-direction: column;
    align-items: flex-start;

    .name {
      margin-bottom: 20px;
      align-self: flex-start;
      padding: 0px 20px;
      
    }
  }

  a {
    color: #17224d;
    text-decoration: none;
  }

  .name {
    flex-basis: 0;
    font-size: 2rem;
    font-weight: 800;
    line-height: 0.9;
  }

  .nav-items {
    display: flex;
    justify-content: flex-end;
    flex-grow: 2;

    @media (max-width: 500px) {
      padding: 0px 20px;
    }

    a {
      margin: 0 10px;
      color: #aaaaaa;
      font-weight: 500;
      font-size: 16px;

      @media (max-width: 500px) {
        margin: 0px 10px 0px 0px;
      }
    }
    a:hover {
      color: #5220dd;

      @media (max-width: 500px) {
        font-weight: 600;
      }
    }
  }

  .about-nav {
    .is-active {
      color: #5220dd;
      font-weight: 600;
    }
  }

  
}
</style>
