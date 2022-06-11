<script setup>

import item from './components/item.vue'

</script>


<script>
import datos from './datos/services.json'


export default {
  data() {
    return {
      servicio: null
    }
  },

  mounted() {
    this.servicio =   datos;
    console.log(datos)
  },
}
</script>

<template>
  <img alt="Vue logo" style="width:70px" src="./assets/logo.png" />
  <h1> Sea bienvenido(a)!</h1>
<hr/>
  <div class="items">

      <item
        v-for="servici, index in  servicio"
        :key="index"
        :item="servici"
      />
  </div>
 
</template>



<!-- cd likn-services
  npm install
  npm run dev -->

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
html{
  background: url("https://cdn.pixabay.com/photo/2014/08/01/00/08/pier-407252_960_720.jpg") ;
  background-repeat: no-repeat ;
  background-size: cover ;
  min-height: 100%;
}
.items{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>
