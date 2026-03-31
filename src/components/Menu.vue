<template>
    <div class="container">
        <div class="logo">
            <i class="bi bi-tiktok"></i>
            <p>TikTok</p>
        </div>
        <div class="pesquisar">
            <button class="fundo-pesquisar">
                <div class="icone">
                    <i class="bi bi-search"></i>
                </div>
                <div class="texto">
                    <p>Pesquisar</p>
                </div>
            </button>
        </div>
        <div class="menu">
            <ItemMenu v-for="titulo in menus" :titulo="titulo.titulo" :icone="titulo.icone"></ItemMenu>
        </div>
        
    </div>
</template>
<style>
    .container{
        display: flex;
        flex-direction: column;
        align-items: start;
    }
    .logo{
        display: flex;
        flex-direction: row;
    }
    .logo i {
        margin: 5px;
    }
    .logo p {
        margin: 5px;
    }

    .fundo-pesquisar{
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        background-color: gray;
        border: 0px solid ;
         border-radius: 10px;
    }
    .pesquisar :hover{
        background-color: antiquewhite;
        cursor: pointer;
    }
    .fundo-pesquisar i{
        font-size: 11px;
        margin: 0;
        padding: 0;
    }
    .fundo-pesquisar p{
        font-size: 11px;
        margin-right: 5px;
    }

</style>
<script setup lang="ts">
import { ref } from 'vue';
import ItemMenu from './ItemMenu.vue';

const menus = ref([
    {
        titulo: "Para você",
        icone: "bi bi-house"
    },
     {
        titulo: "Explorar",
        icone: "bi bi-search"
    },
    {
        titulo: "Seguindo",
        icone: "bi bi-person-check"
    },
    {
        titulo: "Amigos",
        icone: "bi bi-people"
    },
    {
        titulo: "LIVE",
        icone: "bi bi-tv"
    },
    {
        titulo: "Mensagens",
        icone: "bi bi-chat-left-dots"
    },
])




</script>