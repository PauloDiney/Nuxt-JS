<template>
    <form action="" @submit.prevent="recebaDados">
        <label for="label-nome">Nome:</label>
        <input  v-model="inputNome" type="text" name="nome" id="nome">
        <label for="email">Email:</label>
        <input v-model="inputEmail" type="text" name="email" id="email">

        <label for="mensagem">mensagem: </label>
        <textarea   v-model="inputMensa" name="msg" id="mensagem"></textarea>
        <button>Enviar</button>
    </form>
</template>

<script>
import { dataToEsm } from '@rollup/pluginutils';


 export default{
    data() {
        return{
            inputNome : "Paulo",
            inputEmail: "paulo@gmail.com",
            inputMensa: "Pão"
        }
    },
    methods: {
        recebaDados(){
            const dados = {
                nome: this.inputNome,
                email: this.inputEmail,
                msg: this.inputMensa,
            }
            this.$emit("enviarDados", dados)
        }
    }
 }
</script>