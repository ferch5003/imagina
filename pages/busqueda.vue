<template>
  <div class="container">
    <div>
      <h1 class="title">Consolidado de Propuestas</h1>
        <div class="columns is-multiline">
        <TarjetaPropuesta :color="color" :propuesta="propuesta" v-for="propuesta in propuestas" :key= "propuesta.id" />
        </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import env from '../config/env.js'
import TarjetaPropuesta from '../components/TarjetaPropuesta.vue'
export default {
  name: 'SearchPage',
  mounted:function(){
    var color = localStorage.getItem('color');
    if(color){
      document.getElementsByClassName('navbar')[0].style.backgroundColor = color;
      this.color = color;
    }
  },
  components: {
    TarjetaPropuesta
  },
  data() {
    return {
      propuestas: [],
      color: 'black'
    }
  },
  created() {
    axios.get(`${env.endpoint}/posts`).then((response) => {
      this.propuestas = response.data
    })
  }
}
</script>

<style scope>

</style>
