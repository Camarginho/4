<template>
    <h1> Pagina de Contato </h1>
    <FormularioContato 
        @enviarDados="receberDados"
    />
    <hr>
    <p> Lista de Contatos: </p>
    <ul v-for="ct in Object.keys(listaContato)">
        <li> Nome: <strong> {{ listaContato[ct].nome }} </strong></li>
        <li> Email: <strong> {{ listaContato[ct].email }} </strong></li>
        <li> Msg: <strong> {{ listaContato[ct].msg }} </strong></li>
        <hr>
    </ul>
</template>

<script>

export default {
    data() {
        return {
            listaContato: [
               
            ]
        }
    },
    methods: {
        receberDados(dados) {
            console.log(dados)
            this.listaContato.push(dados)
        }
    }
}

</script>