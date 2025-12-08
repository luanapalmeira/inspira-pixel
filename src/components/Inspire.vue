<script setup>
import { ref } from "vue";
import Card from "./Card.vue";
//Ele nos permite buscar dados de APIs externas de forma simples.
import axios from "axios";

// Criamos uma variável reativa que vai guardar a lista de imagens.
const imagens = ref([]);

async function carregarImagens() {
    const resposta = await axios.get("https://picsum.photos/v2/list?page=2&limit=10");
    imagens.value = resposta.data;
    console.log(resposta);
}

carregarImagens();
</script>

<template>
    <section>
        <h2>Inspire-se</h2>

        <section class="cards">
            <Card v-for="img in imagens" :imagem="img.download_url" />
        </section>
    </section>
</template>

<style scoped lang="scss">
    .cards {
        display: flex;
        flex-wrap: wrap;
        gap: 1rem;
        justify-content: center;
    }
</style>