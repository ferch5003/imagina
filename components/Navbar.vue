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
            <a class="navbar-item" @click="propuestas" href="/busqueda">Propuestas</a>
            <a class="navbar-item" @click="showModalLogin = true">Iniciar Sesión</a>
            <a class="navbar-item" @click="showModalRegister = true">Registrarse</a>
          </div>
        </div>
      </nav>
    </div>
    <Login v-if="showModalLogin" @close="showModalLogin = false"></Login>
    <Register v-if="showModalRegister" @close="showModalRegister = false"></Register>
  </div>
</template>

<style>
</style>

<script>
import Login from '../components/Login.vue'
import Register from '../components/Register.vue'

export default {
  name: "Navbar",
  props:{
      bgc: Object
  },
  components :{
    Login,
    Register
  },
  data() {
    return {
      showNav: false,
      showModalLogin : false,
      showModalRegister : false
      };
  },
  methods: {
    propuestas: function(){
      var color = localStorage.getItem('color');
      if(color){
        localStorage.removeItem('color');
      }
    }
  }
};
</script>

<style scope>
.navbar{
  box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
  transition: all 0.3s cubic-bezier(.25,.8,.25,1);
}
.navbar{
  transition: 0.5s;
}
</style>
