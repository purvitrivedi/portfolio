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
  // padding: 0px 0px 0px 39px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;

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
    a {
      margin: 0 10px;
      color: #aaaaaa;
      font-weight: 500;
      font-size: 16px;
    }
    a:hover {
      color: #17224d;
    }
  }

  .about-nav {
    .is-active {
      color: #17224d;
    }
  }
}
</style>
