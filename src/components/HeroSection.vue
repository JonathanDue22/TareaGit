<template>
  <section class="hero">
      <div class="hero-text">
    </div>
  </section>
</template>

<script>
export default {
  name: 'HeroSection'
}
</script>

<style scoped>
.hero {
  background: linear-gradient(135deg, #f4a261 0%, #e76f51 100%);
  padding: 4rem 0;
  color: white;
  position: relative;
  overflow: hidden;
}

.hero::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0,0,0,0.1);
}

.hero-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  position: relative;
  z-index: 2;
}

.exercise-label {
  background: rgba(0,0,0,0.8);
  color: white;
  padding: 0.5rem 1rem;
  font-size: 0.9rem;
  font-weight: bold;
  display: inline-block;
  margin-bottom: 1rem;
}

.hero-text h1 {
  font-size: 2.5rem;
  margin-bottom: 1rem;
  font-weight: 700;
}

.hero-text p {
  font-size: 1.1rem;
  max-width: 600px;
  line-height: 1.6;
  opacity: 0.95;
}

@media (max-width: 768px) {
  .hero-text h1 {
    font-size: 2rem;
  }
  
  .hero-text p {
    font-size: 1rem;
  }
}
</style>