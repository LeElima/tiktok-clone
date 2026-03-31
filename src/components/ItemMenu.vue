<template>
    <div class="linha">
        <div class="icone">
            <i :class="icone"></i>
        </div>
        <div class="texto">
            <p>{{ titulo }}</p>
        </div>
    </div>
</template>
<style>
    .linha{
        display: flex;
        flex-direction: row;
        height: 50px;
    }
    .icone{
       
        display: flex;
        justify-content: center;
        align-items: center;
        margin: 0px 10px 0px 10px;
    }
    .texto{
        display: flex;
        justify-content: center;
        align-items: center;
    }
</style>
<script setup lang="ts">
const props = defineProps({
  titulo: String,
  icone: String,
  pagina: String
})




</script>