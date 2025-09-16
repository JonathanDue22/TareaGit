<!-- components/HeaderComponent.vue -->
<template>
  <header class="header">
    <div class="container">
      <div class="logo-section">
        <!-- El logo ahora es un link -->
        <a href="/">
  <img src="/LogoITCA.png" alt="LogoITCA" class="logo">
</a>

      </div>
      <nav class="navigation">
        <ul class="nav-menu">
          <li><a href="#inicio">Inicio</a></li>
          <li><a href="#nosotros">Nosotros</a></li>
          <li><a href="#carreras">Carreras</a></li>
          <li><a href="#admisiones">Admisiones</a></li>
          <li><a href="#biblioteca">Biblioteca</a></li>
          <li><a href="#contacto">Contacto</a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderComponent'
}
</script>

<style scoped>
.header {
  background: linear-gradient(135deg, #f4a261 0%, #e76f51 100%);
  padding: 1rem 0;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 2rem;
}

.logo {
  height: 50px;
  width: auto;
  cursor: pointer;
}

.nav-menu {
  display: flex;
  list-style: none;
  gap: 2rem;
}

.nav-menu a {
  color: white;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.3s ease;
}

.nav-menu a:hover {
  color: #264653;
}

@media (max-width: 768px) {
  .nav-menu {
    display: none;
  }
}
</style>
