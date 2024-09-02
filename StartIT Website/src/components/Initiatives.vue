<template>
  <section class="initiatives-section">
    <div class="initiatives-container">
      <div class="initiatives-title">
        <h2>Our Initiatives</h2>
      </div>
      <div class="initiatives-content">
        <!-- <p>Initiatives (Scroll Gallery)</p> -->
        <!-- Add your scroll gallery or content here -->
        <carousel :items-to-show="1" :autoplay="5000">
          <slide v-for="(slide, index) in slides" :key="index">
            <div class="carousel__item"><img :src="slide.path" :alt="slide.alt" /></div>
          </slide>
          <template #addons>
            <navigation />
            <pagination />
          </template>
        </carousel>
      </div>
    </div>
  </section>
</template>

<script>
import { Carousel, Navigation, Pagination, Slide } from 'vue3-carousel'

import 'vue3-carousel/dist/carousel.css'

import { ref, computed } from 'vue'
import img1 from "@/assets/IMG_8219.png"
import img2 from '@/assets/IMG_8751.png'

export default {
  name: 'Initiatives',
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation
  },
  setup() {
    const slides = ref([ 
      {path: img1, alt: "BitHacks"},
      {path: img2, alt: "Project X"}
    ])

    return { slides }
  }
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
  max-height: 1000px;
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
  max-height: flex;
}

.initiatives-content p {
  color: #f39c12;
  font-family: 'Poppins', sans-serif;
  font-size: 22px;
  margin: 0;
}

.carousel__item {
  min-height: 200px;
  max-width: 90%;
  max-height: 500px;
  width: 100%;
  overflow: hidden;
  background-color: var(--vc-clr-primary);
  color: var(--vc-clr-white);
  font-size: 20px;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.carousel__item img {
  width: 100%;
  height: auto;
  object-fit: contain; /* or 'cover', depending on the desired effect */
  border-radius: 8px;
}

.carousel__slide {
  padding: 10px;
  max-height: 1000px;
}

.carousel__prev,
.carousel__next {
  box-sizing: content-box;
  border: 5px solid white;
}
</style>
