<template>
  <div id="app">
    <nav id="navbar">
      <Navigation/>
    </nav>
    <router-view style="margin:10px;"/>
  </div>
</template>

<script>
import Navigation from '@/components/Navigation.vue'


export default {
  name: 'App',
  components: {
    Navigation
  }
}
</script>


<style scoped>
#app {
}

#navbar {
  width: 10%;
  padding: 30px;
}

#nav a {
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
