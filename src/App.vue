<template>
  <div id="app">
    <HeaderComponent />
    <HeroSection />
    <AwardsSection />
    <ContenidoComponent></ContenidoComponent>    
    <DescriptionSection />
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import HeroSection from './components/HeroSection.vue'
import AwardsSection from './components/AwardsSection.vue'
import DescriptionSection from './components/DescriptionSection.vue'
import FooterComponent from './components/FooterComponent.vue'
import ContenidoComponent from './components/ContenidoComponent.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    HeroSection,
    AwardsSection,
    DescriptionSection,
    FooterComponent,
    ContenidoComponent
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Arial', sans-serif;
  line-height: 1.6;
  color: #333;
}

#app {
  min-height: 100vh;
}
</style>