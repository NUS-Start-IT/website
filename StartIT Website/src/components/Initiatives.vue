<template>
    <section class="initiatives-section">
      <div class="initiatives-container">
        <div class="initiatives-title">
          <h2>Our Initiatives</h2>
        </div>
        <div class="initiatives-content">
          <p>Initiatives (Scroll Gallery)</p>
          <!-- Add your scroll gallery or content here -->
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'Initiatives'
  }
  </script>
  
  <style scoped>
  .initiatives-section {
    width: 100%;
    background-color: #2c2c2c;
    padding: 50px 0;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: -50px; /* Pulls the section upwards */
    position: relative;
    z-index: 2; /* Ensures it sits above the home section content */
  }
  
  .initiatives-container {
    width: 90%;
    max-width: 1000px;
    background-color: #1e1e1e;
    border-radius: 10px;
    position: relative;
    padding: 50px 20px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
  }
  
  .initiatives-title {
    position: absolute;
    top: -25px;
    left: 50%;
    transform: translateX(-50%);
    background-color: #111;
    padding: 10px 20px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
  }
  
  .initiatives-title h2 {
    margin: 0;
    color: #f39c12;
    font-family: 'Poppins', sans-serif;
    font-size: 24px;
    text-align: center;
  }
  
  .initiatives-content {
    padding: 40px 20px;
    text-align: center;
  }
  
  .initiatives-content p {
    color: #f39c12;
    font-family: 'Poppins', sans-serif;
    font-size: 22px;
    margin: 0;
  }
  </style>
  