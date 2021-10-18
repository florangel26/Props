<template>
  <div>
    <section v-if="arreglo.length === 0">
      <p>Aquí irán las tareas</p>
    </section>
    <section v-else>
      <ul>
        <li v-for="(el,index) in arreglo" :key="index">{{el.tarea}}</li>
      </ul>
    </section>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    arreglo: {
      type: Array,
      default: () => []
    }
  },
}
</script>


<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
li {
  margin: 0 10px;
  font-size: 20px;
  font-weight: bold;
}
p{
  font-size: 20px;
  font-weight: bold;
  color: rgb(33, 128, 145);
}
</style>
