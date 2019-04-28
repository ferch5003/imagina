<template>
  <div class="columns wave-user">
    <figure class="image is-32x32">
      <img src="https://bulma.io/images/placeholders/32x32.png" class="is-rounded"  alt="Placeholder image">
    </figure>
    <p>{{usuario.name}}</p>
  </div>
</template>

<script>
import axios from 'axios'
import env from '../config/env.js'
export default {
  name: 'Users',
  props:{
    usuario:Object
  }
}
</script>

<style scope>
.wave-user{
  margin-left: -30px;
  margin-top: 25px;
}
</style>
