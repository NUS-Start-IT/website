<template>
  <div id="app">
    <Navbar />
    <router-view />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';

export default {
  name: 'App',
  components: {
    Navbar
  }
}
</script>

<style>
body {
  margin: 0;
  font-family: 'Poppins', sans-serif;
  background-color: #000;
  color: #fff;
}

#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
</style>


