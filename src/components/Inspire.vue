<script setup>
import { ref } from "vue";
import Card from "./Card.vue";
//Ele nos permite buscar dados de APIs externas de forma simples.
import axios from "axios";

// Criamos uma variável reativa que vai guardar a lista de imagens.
const imagens = ref([]);

async function carregarImagens() {
    const resposta = await axios.get("https://picsum.photos/v2/list?page=2&limit=12");
    imagens.value = resposta.data;
    console.log(resposta);
}

carregarImagens();
</script>

<template>
    <section class="inspire">
        <h2>Inspire-se</h2>

        <section class="cards">
            <Card v-for="img in imagens" :imagem="img.download_url" />
        </section>
    </section>
</template>

<style scoped lang="scss">
.inspire {
    display: flex;
    flex-direction: column;
    width: 75%;
    margin-top: 6rem;
    margin-bottom: 3rem;
    margin-left: 14rem;

    h2 {
        font-size: 2.5rem;
        font-weight: 400;
        color: #262626;
        margin-left: 1rem;
        margin-bottom: 1.5rem;
    }

    .cards {
        display: flex;
        flex-wrap: wrap;
        gap: 2rem;
        justify-content: center;
    }
}
</style>