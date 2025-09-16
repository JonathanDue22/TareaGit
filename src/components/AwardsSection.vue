<!-- components/AwardsSection.vue -->
<template>
  <section class="awards-section">
    <div class="container">
      <div class="awards-header">
        <h2>PREMIOS Y RECONOCIMIENTOS</h2>
      </div>
      
      <div class="awards-gallery">
        <div class="award-item" v-for="(award, index) in awards" :key="index">
          <img :src="award.image" :alt="award.alt" class="award-image" @error="handleImageError">
          <div class="award-overlay">
            <h3>{{ award.title }}</h3>
            <p>{{ award.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AwardsSection',
  data() {
    return {
      awards: [
       
        {
          image: 'https://www.itca.edu.sv/wp-content/uploads/2024/07/BannerWeb-Carreras-Tecnicas-general.jpg',
          alt: 'Ceremonia de premios institucional',
          title: 'Premios Institucionales',
          description: 'Ceremonia anual de reconocimientos'
        },
        {
          image: 'https://apps.itca.edu.sv/portalestudiantil/img/LATERAL.png',
          alt: 'Competencias técnicas',
          title: 'Competencias Técnicas',
          description: 'Participación en eventos nacionales'
        },
        {
          image: 'https://www.itca.edu.sv/wp-content/uploads/2017/06/teclacentral2017-1.jpg',
          alt: 'Becas académicas',
          title: 'Becas Académicas',
          description: 'Apoyo a estudiantes sobresalientes'
        },    
      ]
    }
  },
  methods: {
    handleImageError(event) {
      // Imagen de respaldo en caso de error
      event.target.src = 'https://via.placeholder.com/400x300/264653/ffffff?text=Premio';
    }
  }
}
</script>

<style scoped>
.awards-section {
  padding: 4rem 0;
  background-color: #f8f9fa;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.awards-header {
  text-align: center;
  margin-bottom: 3rem;
}

.awards-header h2 {
  font-size: 2.5rem;
  color: #264653;
  font-weight: 700;
  position: relative;
  padding-bottom: 1rem;
}

.awards-header h2::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 100px;
  height: 4px;
  background: linear-gradient(90deg, #f4a261, #e76f51);
  border-radius: 2px;
}

.awards-gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.award-item {
  position: relative;
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0,0,0,0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  cursor: pointer;
  background-color: #fff;
}

.award-item:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0,0,0,0.15);
}

.award-image {
  width: 100%;
  height: 200px;
  object-fit: cover;
  transition: transform 0.3s ease;
  padding-top: lazy;
}

.award-item:hover .award-image {
  transform: scale(1.05);
}

.award-overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: linear-gradient(transparent, rgba(0,0,0,0.8));
  color: white;
  padding: 2rem 1.5rem 1.5rem;
  transform: translateY(100%);
  transition: transform 0.3s ease;
}

.award-item:hover .award-overlay {
  transform: translateY(0);
}

.award-overlay h3 {
  font-size: 1.3rem;
  margin-bottom: 0.5rem;
  font-weight: 600;
}

.award-overlay p {
  font-size: 0.9rem;
  opacity: 0.9;
}

@media (max-width: 768px) {
  .awards-gallery {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
  
  .awards-header h2 {
    font-size: 2rem;
  }
}
</style>