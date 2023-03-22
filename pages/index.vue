<template>
  <FormularioContato 
        @enviarDados="receberDados"
    />
    <hr>
    <p> Lista de Nomes: </p>
    <ul v-for="ct in Object.keys(listaContato)">
        <li> Nome: <strong> {{ listaContato[ct].nome }} </strong></li>
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
