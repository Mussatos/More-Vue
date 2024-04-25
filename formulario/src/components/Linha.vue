<script setup>

const props = defineProps(["pessoa"]);

</script>

<template>

    <tr>
        <td>{{ pessoa.nome }}</td>
        <td>{{ pessoa.cpf }}</td>
        <td>{{ pessoa.categoria }}</td>
        <td></td>
        
    </tr>

</template>