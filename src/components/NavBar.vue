<template>
    <div class="navBar">
        <div class="boxLogo">
            <img class="logoRaizen" :src="state.logoImg">    
        </div>
    </div>
</template>



<script setup>
    import { reactive } from 'vue'
    import logo from '../assets/logo.png'

    const state = reactive({
        logoImg: logo
    })


</script>



<style scoped>
    .navBar {
    width: 100vw;
    height: 10vh;
    background-color: #781E77;
    padding: 0 20px;
    display: flex;
    justify-content: center; /* Centraliza a logo horizontalmente */
    align-items: center; /* Centraliza verticalmente */
    }

    .boxLogo {
    width: 10%; /* ou ajuste conforme necessário */
    max-width: 170px; /* limite máximo para telas maiores */
    height: 80%;
    display: flex;
    justify-content: center;
    align-items: center;
    }

    .boxLogo img {
    max-height: 100%; /* A logo não ultrapassa a altura da navbar */
    width: auto; /* A largura será ajustada proporcionalmente */
    object-fit: contain; /* Mantém a proporção da imagem */
    }
</style>