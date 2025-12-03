<script setup>
defineProps(["imagem"]);
</script>

<template>
    <div class="card">
        <!-- Pegar o ícone do coração na biblioteca depois -->
        <button>💗</button>
        <img :src="imagem"
            alt="Imagem ilustrativa">
    </div>
</template>

<style scoped lang="scss">
.card {
    width: 15vw;
    height: 45vh;
    // border: solid;
    position: relative;

    button {
        position: absolute;
        top: 10px;
        right: 10px;
        background-color: transparent;
        border: none;
        font-size: 1.5rem;
    }

    img {
        border-radius: 10px;
        width: 100%;
        height: 100%;
    }
}
</style>