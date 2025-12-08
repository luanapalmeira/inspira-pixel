<script setup>
import { ref } from 'vue';
import { Icon } from "@iconify/vue";

defineProps(["imagem"]);

const likeAtivo = ref(false);

const trocarCor = () => {
    likeAtivo.value = !likeAtivo.value;
};
</script>

<template>
    <div class="card">
        <!-- Pegar o ícone do coração na biblioteca depois -->
        <button class="iconeCoracao" @click="trocarCor">
            <Icon icon="fluent:heart-32-filled" width="35" height="35" :class="{ clicou: likeAtivo }" />
        </button>
        <img :src="imagem" alt="Imagens ilustrativas de paisagens">
    </div>
</template>

<style scoped lang="scss">
.card {
    width: 17vw;
    height: 50vh;
    position: relative;

    button {
        position: absolute;
        top: 12px;
        right: 12px;
        background-color: transparent;
        border: none;
        font-size: 1.5rem;
        color: #FFFFFF;

        .clicou {
            color: #E1306C;
        }
    }

    img {
        border-radius: 10px;
        width: 100%;
        height: 100%;
    }
}
</style>