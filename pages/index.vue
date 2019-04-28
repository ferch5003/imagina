<template>
  <section class="container ">
    <div class="column is-full">
      <h1 class="title">
        Imagina tu ciud&aacute;
      </h1>
      <br>

      <div class="columns box ">
        <div class="column is-one-fifth">
          <a class="button retos is-primary" ref="reto1" id="reto1" @click="retos(1)">Reto 1</a>
        </div>
        <div class="column is-one-fifth">
          <a class="button retos is-success" ref="reto2" id="reto2" @click="retos(2)">Reto 2</a>
        </div>
        <div class="column is-one-fifth">
          <a class="button retos is-warning" ref="reto3" id="reto3" @click="retos(3)">Reto 3</a>
        </div>
        <div class="column is-one-fifth">
          <a class="button retos is-danger" ref="reto4" id="reto4" @click="retos(4)">Reto 4</a>
        </div>
        <div class="column is-one-fifth">
          <a class="button retos is-info" ref="reto5" id="reto5" @click="retos(5)">Reto 5</a>
        </div>
      </div>
      <div class="columns tarjetas">
        <div class="column is-half box tarjeta" @click="showModalRegister = true">
          <div>
            <img src="~/static/leader_360x630.png" class="bordes arcoiris" alt="Placeholder image">
          </div>
          <div class="title">Unete</div>
          <div class="subtitle">a nuestra busqueda de soluciones</div>
        </div>
        <div class="column is-half box tarjeta">
          <div>
            <img src="~/static/urna_160x160.png" class="bordes arcoiris" alt="Placeholder image">
          </div>
          <div class="title">Apoya</div>
          <div class="subtitle">a la idea que mas te guste</div>
        </div>
      </div>
    </div>
  <Register v-if="showModalRegister" @close="showModalRegister = false"></Register>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Register from '~/components/Register.vue'

export default {
  name: 'IndexPage',
  components: {
    Logo,
    Register
  },
  data(){
    return {
      'showModalRegister': false
    }
  },
  methods:{
    retos: function(id){
      switch(id){
        case 1:
          localStorage.setItem('color','#00d1b2');
          break;
        case 2:
          localStorage.setItem('color','#23d160');
          break;
        case 3:
          localStorage.setItem('color','#ffdd57');
          break;
        case 4:
          localStorage.setItem('color','#ff3860');
          break;
        case 5:
          localStorage.setItem('color','#209cee');
          break;
      }
      window.location.replace('/busqueda');
    }
  }
}
</script>

<style scope>
/* Sample `apply` at-rules with Tailwind CSS
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.bordes{
  position: relative;
  padding: 3px;
  border-radius:60% 40% 25% 75% / 32% 40% 60% 68%;
}
.retos{
  position: relative;
  padding: 3px;
  border-radius:60% 40% 19% 81% / 38% 40% 60% 62%
}
.arcoiris{
    background-image: linear-gradient(90deg, #00C0FF 0%, #FFCF00 49%, #FC4F4F 100%);
}
.columns{
  padding-bottom: 20px;
}

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.tarjeta{
  margin-right: 20px;
  height: 450px;
  cursor:pointer;
  box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
  transition: all 0.3s cubic-bezier(.25,.8,.25,1);
}

.tarjetas{
  margin-top: 25px;
}

.tarjeta:hover{
  box-shadow: 0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
