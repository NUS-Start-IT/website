<template>
    <header class="navbar">
      <div class="navbar-container">
        <div class="logo">
          <img src="@/assets/logo.png" alt="StartIT Logo">
        </div>
        <nav>
          <ul>
            <li>
              <router-link 
                :to="{ name: 'Home' }"
                :class="{ active: $route.name === 'Home' }"
              >Home</router-link>
            </li>
            <li>
              <router-link 
                :to="{ name: 'AboutUs' }"
                :class="{ active: $route.name === 'AboutUs' }"
              >About Us</router-link>
            </li>
            <li>
              <router-link 
                :to="{ name: 'Contact' }"
                :class="{ active: $route.name === 'Contact' }"
              >Contact</router-link>
            </li>
          </ul>
        </nav>
      </div>
    </header>
  </template>
  
  <script>
  export default {
    name: 'Navbar',
  }
  </script>
  
  <style scoped>
  .navbar {
    width: 100%;
    background-color: #000;
    display: flex;
    justify-content: center;
  }
  
  .navbar-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    max-width: 1200px;
    padding: 20px 50px;
  }
  
  .logo img {
    width: 100px;
  }
  
  nav ul {
    list-style: none;
    display: flex;
    margin: 0;
    padding: 0;
  }
  
  nav ul li {
    margin: 0 20px;
  }
  
  nav ul li a {
    text-decoration: none;
    color: gray; /* Default color */
    font-size: 16px;
    font-family: 'Poppins', sans-serif;
    text-align: center;
  }
  
  nav ul li a.active {
    color: white; /* Active link color */
  }
  
  nav ul {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  </style>
  