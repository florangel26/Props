<template>
  <div id="app">
    <label>Tarea</label>
    <input v-model="tarea" type="text" placeholder="Ingrese nueva tarea">
    <button @click="ingresarTarea()">Añade</button>
    <HelloWorld :arreglo="miarreglo"/>
  </div>
  
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'
export default {
  
  name: 'App',
  data() {
    return {
      miarreglo: [],
      tarea: "",
    }
  },
  components: {
    HelloWorld,
  },
  methods: {
    ingresarTarea() {
      if(!this.tarea) return
      this.miarreglo.push({tarea: this.tarea})
      this.tarea = ""
    }
  },
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
label{
  font-size: 20px;
  margin: 0 10px;
  font-weight: bold;
}
input{
  padding: 5px;
  border-radius: 4px;
  border: 1px solid #ddd;
}
button{
  width: 6%;
  padding: 4px;
  border-radius: 4px;
  border: 2px solid #6256f0;
  margin: 0 5px;
  background-color: #fff;
  color: #7d96df;
  border-color:#7d96df;
;
  cursor: pointer;
}

</style>
