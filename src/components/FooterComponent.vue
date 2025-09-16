<!-- components/FooterComponent.vue -->
<template>
  <footer class="footer">
      
    
  </footer>
</template>

<script>
export default {
  name: 'FooterComponent'
}
</script>

<style scoped>
.footer {
  text-align: center;
  background: linear-gradient(135deg, #264653 0%, #2a9d8f 100%);
  color: white;
  padding: 3rem 0 1rem;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 2rem;
  margin-bottom: 2rem;
}

.footer-section h4 {
  font-size: 1.2rem;
  font-weight: 600;
  margin-bottom: 1rem;
  color: #f4a261;
  border-bottom: 2px solid #f4a261;
  padding-bottom: 0.5rem;
}

.footer-section ul {
  list-style: none;
}

.footer-section li {
  margin-bottom: 0.5rem;
}

.footer-section a {
  color: rgba(255,255,255,0.8);
  text-decoration: none;
  font-size: 0.9rem;
  transition: color 0.3s ease, padding-left 0.3s ease;
  display: block;
  padding: 0.2rem 0;
}

.footer-section a:hover {
  color: #f4a261;
  padding-left: 0.5rem;
}

.footer-bottom {
  border-top: 1px solid rgba(255,255,255,0.2);
  padding-top: 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.footer-logos {
  display: flex;
  align-items: center;
  gap: 2rem;
}

.footer-logo {
  height: 40px;
  width: auto;
  filter: brightness(0) invert(1);
}

.social-links {
  display: flex;
  gap: 1rem;
}

.social-link {
  width: 40px;
  height: 40px;
  background: rgba(255,255,255,0.1);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  text-decoration: none;
  font-size: 1.2rem;
  transition: all 0.3s ease;
}

.social-link:hover {
  background: #f4a261;
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(244, 162, 97, 0.3);
}

.footer-info {
  text-align: right;
}

.footer-info p {
  font-size: 0.8rem;
  opacity: 0.8;
  margin-bottom: 0.3rem;
}

@media (max-width: 768px) {
  .footer-content {
    grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem;
  }
  
  .footer-bottom {
    flex-direction: column;
    gap: 1rem;
    text-align: center;
  }
  
  .footer-info {
    text-align: center;
  }
}

@media (max-width: 480px) {
  .footer-content {
    grid-template-columns: 1fr;
  }
  
  .footer-logos {
    flex-direction: column;
    gap: 1rem;
  }
}
</style>