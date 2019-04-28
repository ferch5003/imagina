<template>
  <div>
    <div class="hero-head">
      <nav class="navbar">
        <div class="navbar-brand">
          <a class="navbar-item" href="/">
            <img src="http://bulma.io/images/bulma-logo.png" alt="Logo">
          </a>
          <div class="navbar-burger" @click="showNav = !showNav" :class="{ 'is-active': showNav }">
            <span></span>
            <span></span>
            <span></span>
          </div>
        </div>
        <div class="navbar-menu" :class="{ 'is-active': showNav }">
          <div class="navbar-end">
            <a class="navbar-item" href="/busqueda">Propuestas</a>
            <a class="navbar-item" @click="showModal = true">Iniciar Sesión</a>
          </div>
        </div>
      </nav>
    </div>
    <Login v-if="showModal" @close="showModal = false"></Login>
  </div>
</template>

<style>
</style>

<script>
import Login from '../components/Login.vue'

export default {
  name: "Navbar",
  components :{
    Login
  },
  data() {
    return { 
      showNav: false,
      showModal : false
      };
  }
};
</script>