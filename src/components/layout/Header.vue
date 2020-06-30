<template>
  <div class="nav">
    <router-link to="/" class="name">Purvi Trivedi</router-link>
    <div class="nav-items">
      <router-link to="/about">About</router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="scss">
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-bottom: 1px solid black;

  a {
    color: black;
    text-decoration: none;
  }

  .name {
    font-size: 50px;
  }
}
</style>
