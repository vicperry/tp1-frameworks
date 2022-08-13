<template>
  <div id='App'>
  <h1>{{title}}</h1>
  <div class="lista" v-bind:key="task.id" v-for="task in tasks">
    <p v-if="task.estaCompleta == true" id="completa">{{task.descricao}}</p>
    <p v-else id="incompleta">{{task.descricao}}</p>

  </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data: function(){
    return{
    title: "Lista de Tarefas",
    tasks: [
      {id: 1, descricao: "Arrumar a cama", estaCompleta: false},
      {id: 2, descricao: "Escovar os dentes", estaCompleta: true},
      {id: 3, descricao: "Tomar café-da-manhã", estaCompleta: true}
    ]
    }
  }
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

ul{
    list-style-type: none;
}

#completa{
  text-decoration: line-through;
}
</style>
