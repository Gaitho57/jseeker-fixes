<template>
  <div class="landing-page">
    <HeroSection />
    <FeatureBase />
  </div>
</template>

<script setup>
import HeroSection from '@/components/HeroSection.vue';
import FeatureBase from '@/components/FeatureBase.vue';
</script>

<style scoped>
.landing-page {
  min-height: 100vh;
  margin: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  background: #f0f2f5; /* Light background color for the page */
  padding: 20px;
  box-sizing: border-box;
}

/* HeroSection styles */
.hero-section {
  width: 100%;
  background: rgba(255, 255, 255, 0.3); /* Glass-like effect */
  backdrop-filter: blur(15px); /* Glass effect */
  border-radius: 15px;
  padding: 50px 20px;
  box-shadow: 0 8px 32px rgba(31, 38, 135, 0.37); /* Soft shadow */
  border: 1px solid rgba(255, 255, 255, 0.18); /* Transparent border */
  margin-bottom: 20px;
  text-align: center;
}

/* FeatureBase styles */
.feature-base {
  width: 100%;
  max-width: 1200px;
  background: rgba(255, 255, 255, 0.3); /* Glass-like effect */
  backdrop-filter: blur(15px); /* Glass effect */
  border-radius: 15px;
  padding: 40px 20px;
  box-shadow: 0 8px 32px rgba(31, 38, 135, 0.37); /* Soft shadow */
  border: 1px solid rgba(255, 255, 255, 0.18); /* Transparent border */
  text-align: center;
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .hero-section,
  .feature-base {
    padding: 30px 10px;
  }
}

@media (max-width: 480px) {
  .hero-section,
  .feature-base {
    padding: 20px 5px;
  }
}
</style>

