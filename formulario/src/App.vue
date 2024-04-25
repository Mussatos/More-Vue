<script setup>
import Tabela from "./components/Tabela.vue"
import Formulario from "./components/Formulario.vue"
const dados = [
  {
    nome: "Antonio Mussato",
    cpf: "000.111.222-33",
    categoria: "A"
  },
  {
    nome: "Lian Miranda",
    cpf: "222.222.333-44",
    categoria: "B"
  },
  {
    nome: "Vinicius Azambuja",
    cpf: "333.444.555-66",
    categoria: "C"
  },
]

const handleFormulario = (nome, cpf, categoria) =>{
    alert(`Cheguei dentro de APP! ${nome} ${cpf} ${categoria}`);
}

</script>

<template>
  <main>
    <Formulario @salvar-pessoa ="handleFormulario"/>
    <Tabela :pessoas="dados"/> 

  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
