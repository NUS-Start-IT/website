<template>
    <header class="navbar">
      <div class="navbar-container">
        <div class="logo">
          <router-link
            :to="{ name: 'Home' }">
            <img src="@/assets/logo.png" alt="StartIT Logo">
          </router-link>

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
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 80px; /* Reduced height */
  z-index: 1000;
  background-color: #000; /* or whatever your navbar background color is */
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1); /* Optional: add a shadow for better visibility */
}

.navbar-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  /* max-width: 1200px; */
  max-width: 90%;
  padding: 10px 30px; /* Reduced padding */
}

.logo img {
  width: 100px; /* Adjust logo size if needed */
  margin-left: 75px;
}

nav ul li a {
  font-size: 14px; /* Adjust font size if needed */
  padding: 5px 10px; /* Adjust link padding if needed */
}


  nav ul {
    list-style: none;
    display: flex;
    margin: 0;
    padding: 0;
  }
  
  nav ul li {
    margin: 0 20px;
    margin-bottom: 20px;
  }
  
  nav ul li a {
    text-decoration: none;
    color: gray; /* Default color */
    font-size: 16px;
    font-family: 'Poppins', sans-serif;
    text-align: center;
    margin-bottom: -20px;
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

  @media (max-width: 768px) {
    .navbar-container {
      padding: 20px;
      font-size: 10px;
    }

    nav ul li {
    margin: 0 0px;
  }

    nav ul li a {
      text-decoration: none;
      color: gray; /* Default color */
      font-size: 16px;
    }

    .logo img {
      width: 100px; /* Adjust logo size if needed */
      margin-left: 12px;
    }


  }


  
  </style>
  