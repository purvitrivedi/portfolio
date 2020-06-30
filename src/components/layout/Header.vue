<template>
  <div class="nav">
    <h1>Purvi Trivedi</h1>
    <div class="nav-items">
      <router-link to="/">Home</router-link> |
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
}
</style>
