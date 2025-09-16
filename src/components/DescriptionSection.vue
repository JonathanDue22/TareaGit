<!-- components/FooterComponent.vue -->
<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-section">
          <h4>ACERCA</h4>
          <ul>
            <li><a href="#historia">Historia</a></li>
            <li><a href="#mision">Misión y Visión</a></li>
            <li><a href="#autoridades">Autoridades</a></li>
            <li><a href="#campus">Campus</a></li>
            <li><a href="#organigrama">Organigrama</a></li>
            <li><a href="#transparencia">Transparencia</a></li>
          </ul>
        </div>
        
        <div class="footer-section">
          <h4>ESTUDIANTES</h4>
          <ul>
            <li><a href="#admisiones">Admisiones</a></li>
            <li><a href="#becas">Becas</a></li>
            <li><a href="#calendario">Calendario Académico</a></li>
            <li><a href="#servicios">Servicios Estudiantiles</a></li>
            <li><a href="#biblioteca">Biblioteca</a></li>
            <li><a href="#aula-virtual">Aula Virtual</a></li>
          </ul>
        </div>
        
        <div class="footer-section">
          <h4>CARRERAS</h4>
          <ul>
            <li><a href="#tecnicas">Carreras Técnicas</a></li>
            <li><a href="#tecnologicas">Carreras Tecnológicas</a></li>
            <li><a href="#especializaciones">Especializaciones</a></li>
            <li><a href="#educacion-continua">Educación Continua</a></li>
            <li><a href="#modalidades">Modalidades de Estudio</a></li>
            <li><a href="#certificaciones">Certificaciones</a></li>
          </ul>
        </div>
        
        <div class="footer-section">
          <h4>SERVICIOS</h4>
          <ul>
            <li><a href="#laboratorios">Laboratorios</a></li>
            <li><a href="#practicas">Prácticas Profesionales</a></li>
            <li><a href="#bolsa-trabajo">Bolsa de Trabajo</a></li>
            <li><a href="#consultoria">Consultoría</a></li>
            <li><a href="#investigacion">Investigación</a></li>
            <li><a href="#extension">Extensión Social</a></li>
          </ul>
        </div>
      </div>

       <div class="footer-info">
          <p>&copy; 2024 Instituto Tecnológico Centroamericano ITCA. Todos los derechos reservados.</p>
          <p>San Salvador, El Salvador | Teléfono: (503) 2276-8888 | Email: info@itca.edu.sv</p>
        </div>
      </div>
  </footer>
</template>

<script>
export default {
  name: 'FooterComponent'
}
</script>

<style scoped>
.footer {
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