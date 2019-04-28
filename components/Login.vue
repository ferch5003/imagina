<template>
    <transition name="modal">
    <div class="modal-mask">
        <div class="modal">
            <div class="modal-background"></div>
            <div class="modal-card">
                <header class="modal-card-head">
                    <p class="modal-card-title">Iniciar Sesión</p>
                    <button class="delete" @click="$emit('close')" aria-label="close"></button>
                </header>
                <section class="modal-card-body">
                    <div class="field">
                        <label class="label">Correo</label>
                        <div class="control">
                            <input class="input" v-model="correo" type="email" placeholder="Digite correo">
                        </div>
                    </div>

                    <div class="field">
                        <label class="label">Contraseña</label>
                        <div class="control">
                            <input class="input" v-model="pass" type="password" placeholder="Digite la contraseña">
                        </div>
                    </div>
                </section>
                <footer class="modal-card-foot">
                    <button class="button is-success">Iniciar sesión</button>
                    <button class="button" @click="$emit('close')">Cancelar</button>
                </footer>
            </div>
        </div>
    </div>
  </transition>
</template>

<script>
export default {
    name: 'Login',
    data(){
      return {
        'correo': '',
        'pass': ''
      }
    }
}
</script>

<style>
.modal-mask {
  position: fixed;
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, .1);
  display: table;
  transition: opacity .3s ease;
}

.modal{
    padding-top: 10%;
    display: table-cell;
    background-color: rgba(0, 0, 0, .1);
    vertical-align: middle;
    z-index: 9999;
    transition: opacity .3s ease;
}

.modal-wrapper {
  
}

.modal-container {
  width: 300px;
  margin: 0px auto;
  padding: 20px 30px;
  background-color: #fff;
  border-radius: 2px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, .33);
  transition: all .3s ease;
  font-family: Helvetica, Arial, sans-serif;
}

.modal-header h3 {
  margin-top: 0;
  color: #42b983;
}

.modal-body {
  margin: 20px 0;
}

.modal-default-button {
  float: right;
}

/*
 * The following styles are auto-applied to elements with
 * transition="modal" when their visibility is toggled
 * by Vue.js.
 *
 * You can easily play with the modal transition by editing
 * these styles.
 */

.modal-enter {
  opacity: 0;
}

.modal-leave-active {
  opacity: 0;
}

.modal-enter .modal-container,
.modal-leave-active .modal-container {
  -webkit-transform: scale(1.1);
  transform: scale(1.1);
}
</style>
