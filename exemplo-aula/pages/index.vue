<template>
  <div class="container"> 
    <h1>{{titulo}}</h1>
    <ul>
      <li :key="item.id" v-for="item in pessoas">
        {{item.nome}} - Idade: {{item.idade}} anos
      </li>
    </ul>
    <button @click="digaOla">Diga Olá!</button>
  </div>
</template>

<script>
export default{
  data: function(){
    return{
      titulo: "Lista de Pessosas e Idades",
      pessoas: [
        {id: 1,none: "Marcio", idade: "33"},
        {id: 2,none: "Diego", idade: "44"},
        {id: 3,none: "Luana", idade: "50"},
        {id: 4,none: "Tamara", idade: "23"},
      ]
    }
  },
  methods:{
    digaOla: function(){
      alert("Olá Mundo do Nuxt.js!")
    }
  }
}
</script>

<style scoped>
.container{
  margin: 20px;
}
</style>