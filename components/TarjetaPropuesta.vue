<template>
  <div class="box  is-one-quarter column">
    <h3>{{ propuesta.title }}</h3>
  </div>
</template>

<script>
export default {
  name: 'TarjetaPropuesta',
  props: {
    propuesta: Object
  }
}
</script>

<style scope>
.box{

  margin:1em;
}
</style>
