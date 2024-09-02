<template>
  <section class="home">
    <div class="home-content">
      <div class="home-text">
        <h1>NUS StartIT</h1>
        <h2>NUS Computing Technopreneurship Society</h2>
        <p>Providing a platform for Today's Thinkers and Tomorrow's Technopreneurs.</p>
      </div>
      <div class="home-image">
        <img src="@/assets/astronaut.png" alt="Astronaut">
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HomeSection'
}
</script>

<style scoped>
.home {
  width: 100%;
  background-color: #000;
  display: flex;
  justify-content: center;
}

.home-content {
  display: flex;
  align-items: center;
  max-width: 1200px;
  padding: 50px;
}

.home-text {
  flex: 1;
  text-align: left;
  color: #fff;
  font-family: 'Poppins', sans-serif; /* Apply Poppins font here */
}

.home-text h1 {
  font-size: 60px;
  margin: 0;
  color: #f39c12;
}

.home-text h2 {
  font-size: 24px;
  margin: 10px 0;
  color: #e0e0e0;
}

.home-text p {
  font-size: 18px;
  color: #b0b0b0;
}

.home-image {
  flex: 1;
  text-align: right;
}

.home-image img {
  width: 80%;
  height: auto;
}
</style>
