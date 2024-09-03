
<template>
  <section class="contact-us-section">
    <div class="contact-us-container">
      <div class="contact-us-title">
        <h2>Contact Us</h2>
      </div>
      <div class="contact-options">
        <div class="contact-option" v-for="contact in contacts" :key="contact.name">
          <div class="icon">
            <font-awesome-icon :icon="contact.icon" />
          </div>
          <div class="contact-info">
            <strong>{{ contact.name }}</strong>
            <p><a :href="contact.link" target="_blank">{{ contact.username }}</a></p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Contact',
  data() {
    return {
      contacts: [
        {
          name: 'Telegram',
          username: '@NUSStartIT',
          link: 'https://t.me/nusstartit',
          icon: ['fab', 'telegram']
        },
        {
          name: 'Instagram',
          username: '@NUSStartIT',
          link: 'https://instagram.com/nusstartit',
          icon: ['fab', 'instagram']
        },
        {
          name: 'LinkedIn',
          username: 'NUSStartIT',
          link: 'https://linkedin.com/in/nusstartit',
          icon: ['fab', 'linkedin']
        }
      ]
    };
  }
}
</script>

<style scoped>
.contact-us-section {
  width: 100%;
  background-color: #1e1e1e;
  padding: 50px 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

.contact-us-container {
  width: 90%;
  max-width: 1000px;
  position: relative;
}

.contact-us-title {
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

.contact-us-title h2 {
  margin: 0;
  color: #f39c12;
  font-family: 'Poppins', sans-serif;
  font-size: 24px;
}

.contact-options {
  display: flex;
  justify-content: center;
  gap: 20px;
  margin-top: 60px;
}

.contact-option {
  display: flex;
  align-items: center;
  background-color: #2c2c2c;
  border-radius: 10px;
  padding: 10px 20px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
  width: 200px;
}

.icon {
  font-size: 24px;
  color: #f39c12;
  margin-right: 15px;
}

.contact-info {
  display: flex;
  flex-direction: column;
}

.contact-info strong {
  color: #f39c12;
  font-family: 'Poppins', sans-serif;
  font-size: 16px;
}

.contact-info p a {
  color: #b0b0b0;
  font-family: 'Poppins', sans-serif;
  font-size: 14px;
  text-decoration: none;
}

.contact-info p a:hover {
  color: #f39c12;
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
