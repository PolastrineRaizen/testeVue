<template>
    <NavBar/>
    <div class="contentBox">
        <div class="tableCMO">
            <TableCMO :dados="tableDados" :colunas="['Nome','Idade','Altura']" />
        </div>
        <div class="fomularioCMO">

        </div>
    </div>
</template>


    
<script setup>
    import NavBar from '../components/NavBar.vue'
    import TableCMO from '../components/TableCMO'

    const tableDados = [
        {'Data': '2024-12-23','Nome': 123, 'Idade': 25},
        {'Nome': 22, 'Idade': 51, 'Altura': 254},
        {'Nome': 25, 'Idade': 121, 'Altura': 64},
        {'Nome': 672, 'Idade': 44, 'Altura': 82}
    ] // Os dados devem chegar em chaves que representem as colunas criadas utilizar o componente "TableCMO"

    async function fetchCMO() {
        
        
    }
</script>



<style>
    .contentBox{
        width: 100vw;
        height: 100vh;
        display: flex;
        flex-direction: row;
    }
</style>