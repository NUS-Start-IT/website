<template>
    <div class="home">
      <HomeSection />
      <Initiatives />
    </div>
  </template>
  
  <script>
  import HomeSection from '@/components/HomeSection.vue';
  import Initiatives from '@/components/Initiatives.vue';
  
  export default {
    name: 'Home',
    components: {
      HomeSection,
      Initiatives
    }
  }
  </script>
  
  <style scoped>
  .home {
    font-family: 'Poppins', sans-serif;
  }
  </style>
  