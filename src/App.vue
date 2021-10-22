<template>
  <div id="app">
    <top-bar></top-bar>
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>

<script>
import TopBar from './components/content/TopBar.vue'

export default {
  name: 'App',
  components: {
    TopBar
  }
}
</script>

<style scoped>
@import './assets/css/base.css';

#app {
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}

#nav {
  text-align: center;
}

</style>
