<template>
  <div class="hello">
    <ul>
      <li v-for="tarefa in tarefas" v-bind:key="tarefa.id">
        <p v-if="tarefa.estaCompleta == false" id="fazer">
          {{ tarefa.descricao }}
        </p> 
        <p v-if="tarefa.estaCompleta == true" id="feito">
          {{ tarefa.descricao }}
        </p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {},
  data: function(){
    return {
      tarefas: [
        {id: 1, descricao: "Lavar a louça", estaCompleta: false},
        {id: 2, descricao: "Arrumar a cama", estaCompleta: false},
        {id: 3, descricao: "Ir no mercado", estaCompleta: true}
      ]
    }
  }
}
</script>

<style scoped>
#fazer {
  color: red;
}
#feito {
  color: aqua;
}
</style>
