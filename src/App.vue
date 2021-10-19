<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style scoped>
#app {
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
