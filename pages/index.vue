<template>
  <form action="" @submit.prevent="recebaDados">
    <input v-model="inputNome" type="text" name="nome" id="name">
    <button>Adicionar</button>
  </form>

  <div>
    <ul v-for="ct in name">
        <li>Nome: <strong>{{ ct }}</strong></li>
    </ul>
  </div>
</template>

<script>

export default {
  data() {
    return{
      name: [],
      inputNome: ""
    }
    
  },
  methods:{
    recebaDados(){
      this.name.push(this.inputNome)
    }
  }
}


</script>