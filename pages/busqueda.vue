<template>
  <div class="container">
    <div>
      <h1 class="title">Consolidado de Propuestas</h1>
        <div class="columns is-multiline">
        <TarjetaPropuesta :propuesta="propuesta" v-for="propuesta in propuestas" :key= "propuesta.id" />
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
  components: {
    TarjetaPropuesta
  },
  data() {
    return {
      propuestas: []
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
