<template>
  <div>
    <b-button v-b-modal.modal-1>Launch demo modal</b-button>
    <b-modal hide-footer id="modal-1" title="Tabla de calculo">
      <Tabla />
    </b-modal>
  </div>
</template>

<script>
import Tabla from './components/Tabla.vue'

export default {
  name: 'App',
  components: { Tabla }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.close {
  border: none;
  border-radius: 2px;
  background: green;
  color: #fff;
}
</style>
