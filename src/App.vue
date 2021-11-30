<template>
  <div class="container">
    <Navbar/>
    <router-view class="espacio.contenido"/>
<Footer/>
  </div>
  
</template>

<script>
  import Footer from './components/Footer.vue'
  import Navbar from './components/Navbar.vue'

export default {
 components :{
   Navbar,Footer
 }
}
</script>

<style>
.espacio.contenido{
 padding-bottom: 20px; 
 padding-top: 20px;
}
</style>
