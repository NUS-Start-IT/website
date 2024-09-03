<template>
  <section class="intro-section">
    <div class="intro-container">
      <div class="about-us-title">
        <h2>Who We Are</h2>
        <p>
          We are a community of action-takers, driven by the love for IT and technopreneurship. Our
          student-initiated group is the ultimate platform for individuals seeking to explore the
          world of tech and entrepreneurship while gaining essential skills and knowledge in the
          process.
        </p>
      </div>
      <div class="about-us-title">
        <h2>Our Mission</h2>
        <p>
          <strong>Learning</strong> - Immerse yourself in diverse tech fields and entrepreneurship
        </p>
        <p><strong>Sharing</strong> - Grow in a supportive environment</p>
        <p>
          <strong>Networking</strong> - Connect with seasoned entrepreneurs, potential business
          partners, and like-minded peers
        </p>
      </div>
      <div class="about-us-title">
        <h2>Our Vision</h2>
        <p>
          To inspire today's thinkers to become tomorrow's technopreneurs, driving innovation and
          transforming ideas into reality.
        </p>
      </div>
    </div>
  </section>
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
          needed
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
        { name: 'Aryan', role: 'Vice-President', photo: 'path/to/photo4.png' }
        // Add more members as
      ]
    }
  }
}
</script>

<style scoped>
.intro-section {
  width: 100%;
  background-color: black;
  padding: 10px 0;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 80px;
}

.intro-container {
  width: 90%;
  max-width: 1000px;
  position: relative;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
  margin-top: 60px;
}

.about-us-section {
  width: 100%;
  background-color: #1e1e1e;
  padding: 50px 0;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 80px;
}

.about-us-container {
  width: 90%;
  max-width: 1000px;
  position: relative;
}

.about-us-title {
  position: relative;
  top: 0px;
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

.about-us-title p {
  text-align: justify;
  margin: 10px;
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
  margin: 
  0;
}

/* .about-us-title p {
  text-align: justify;
  margin: 10px 0;
  line-height: 1.6;

} */

.about-us-title p {
  text-align: center; /* Aligns text to the left, removing the uneven spacing */
  margin: 10px 0; /* Maintain uniform margins */
  line-height: 1.6; /* Consistent line spacing for readability */
}


/* Mobile-specific styles */
@media (max-width: 768px) {
  .contact-us-title {
    top: -20px;
    padding: 8px 16px;
    font-size: 20px;
    margin-bottom: 0px;
  }

  .contact-options {
    margin-top: 60px;
  }

  .contact-option {
    flex-direction: column;
    align-items: flex-start;
    padding: 15px;
  }

  .icon {
    margin-right: 0;
    margin-bottom: 10px;
  }

  .contact-info strong {
    font-size: 16px;
  }

  .contact-info p a {
    font-size: 14px;
  }
}
</style>
