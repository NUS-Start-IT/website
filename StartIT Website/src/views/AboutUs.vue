<template>
    <section class="about-us-section">
      <div class="about-us-container">
        <div class="about-us-title">
          <h2>Introducing The Committee</h2>
        </div>
        <div class="committee-grid">
          <div class="committee-member" v-for="member in committeeMembers" :key="member.name">
            <div class="member-photo">
              <!-- Placeholder for the member's photo -->
              <img :src="member.photo" alt="Committee Member Photo" />
            </div>
            <div class="member-info">
              <strong>{{ member.name }}</strong>
              <p>{{ member.role }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'AboutUs',
    data() {
      return {
        committeeMembers: [
          { name: 'Aryan', role: 'President', photo: 'path/to/photo1.png' },
          { name: 'Aryan', role: 'Vice-President', photo: 'path/to/photo2.png' },
          { name: 'Aryan', role: 'Vice-President', photo: 'path/to/photo3.png' },
          { name: 'Aryan', role: 'Vice-President', photo: 'path/to/photo4.png' },
          // Add more members as needed
        ]
      };
    }
  }
  </script>
  
  <style scoped>
  .about-us-section {
    width: 100%;
    background-color: #1e1e1e;
    padding: 50px 0;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .about-us-container {
    width: 90%;
    max-width: 1200px;
    position: relative;
  }
  
  .about-us-title {
    position: absolute;
    top: -25px;
    left: 50%;
    transform: translateX(-50%);
    background-color: #111;
    padding: 10px 20px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
    text-align: center;
  }
  
  .about-us-title h2 {
    margin: 0;
    color: #f39c12;
    font-family: 'Poppins', sans-serif;
    font-size: 24px;
  }
  
  .committee-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    margin-top: 60px;
  }
  
  .committee-member {
    background-color: #2c2c2c;
    border-radius: 10px;
    text-align: center;
    padding: 20px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
  }
  
  .member-photo img {
    width: 100%;
    height: auto;
    border-radius: 10px;
    background-color: #ccc; /* Placeholder color for the image */
  }
  
  .member-info {
    margin-top: 10px;
  }
  
  .member-info strong {
    color: #f39c12;
    font-family: 'Poppins', sans-serif;
    font-size: 18px;
  }
  
  .member-info p {
    color: #b0b0b0;
    font-family: 'Poppins', sans-serif;
    font-size: 16px;
    margin: 0;
  }
  </style>
  