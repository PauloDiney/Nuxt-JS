<template>
    <h1>
        <div>Matheus</div> 
       <FormularioContato 
        @enviarDados="recebaDados"
        />
    </h1>

    <hr>
    <p>Lista de contatos:</p>
    <ul v-for="ct in Object.keys(listaContato)">
        <li>Nome: <strong>{{ listaContato[ct].nome }}</strong></li>
        <li>Email: <strong>{{ listaContato[ct].email }}</strong></li>
        <li>Mensagem <strong>{{ listaContato[ct].msg }}</strong></li>
    </ul>
</template>

<script>

export default{
    data(){
        return{
            listaContato: []
        }
    },
    methods: {
        recebaDados(dados){
            console.log(dados)
            this.listaContato.push(dados)
        }
    }
}

</script>