<template>
  <div class="nav">
    <router-link to="/" class="name">Purvi Trivedi</router-link>
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
      >
        <a>{{ type }}</a>
      </router-link>
      <router-link to="/about"><a>About</a></router-link>
    </div>
    <div class="headline">
      Software engineer with experience in UX research.
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      types: ['Code', 'User Research', 'Music']
    }
  }
}
</script>

<style lang="scss">
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  height: 200px;
  // position: fixed;
  // left: 0;
  // top: 0;
  // width: 100vw;
  // z-index: 200;

  // background-color: white;

  .nav-items a {
    margin: 0 5px;
  }

  a {
    color: black;
    text-decoration: none;
  }

  .name {
    font-size: 50px;
  }

  .headline {
    width: 100%;
  }
}
</style>
