<template>
  <div id="app">
    <NavBar />
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;  
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #ccac0b;
}

#nav a.router-link-exact-active {
  color: #678a06;
}
</style>
<script>
import NavBar from './components/NavBar.vue'
export default {
  name: 'Home',
  components: {
    NavBar
  }
}
</script>