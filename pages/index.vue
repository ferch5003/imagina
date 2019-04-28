<template>
  <section class="container ">
    <div class="column is-full">
      <h1 class="title">
        Imagina tu ciud&aacute;
      </h1>
      <br>
      
<div class="columns">
  <div class="column is-one-fifth">
    <a class="button is-primary">reto 1</a>
  </div>
  <div class="column is-one-fifth">
    <a class="button is-success">reto 2</a>
  </div>
  <div class="column is-one-fifth">
    <a class="button is-warning">reto 3</a>
  </div>
  <div class="column is-one-fifth">
    <a class="button is-danger">reto 4</a>
  </div>
  <div class="column is-one-fifth">
    <a class="button is-info">reto 5</a>
  </div>
</div>
<div class="columns">
  <div class="column is-half box">
    <div  >
    <img src="~/static/leader_360x630.png" class="bordes" alt="Placeholder image">
    </div>
    <div class="title">Unete</div>
    <div class="subtitle">a nuestra busqueda de soluciones</div>
  </div>
  <div class="column box">
    <div >
      <img src="~/static/urna_160x160.png" class="bordes" alt="Placeholder image">
    </div>
    <div class="title">Apoya</div>
    <div class="subtitle">a la idea que mas te guste</div>
  </div>
</div>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  name: 'IndexPage',
  components: {
    Logo
  }
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.bordes{
  border-radius:50px;
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
