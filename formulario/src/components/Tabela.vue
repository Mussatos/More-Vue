<script setup>
import Linha from "./Linha.vue";
const props = defineProps(["pessoas"]);

</script>


<template>
    <table>
        <thead>
            <th>Nome</th>
            <th>CPF</th>
            <th>Categoria</th>
            <th>Ações</th>
        </thead>

        <tbody>
            <Linha v-for="item in pessoas"
            :pessoa ="item"/>

           
        </tbody>
    </table>
</template>