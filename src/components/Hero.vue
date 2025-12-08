<script setup></script>

<template>
    <section class="hero">
        <div>
            <h2>Onde a paisagem vira <span>inspiração</span>.</h2>
            <p>Explore paisagens, cores e luzes que inspiram novas histórias através da fotografia.</p>
        </div>

        <img src="../assets/fotografa.png" alt="Imagem ilustrativa de uma fotógrafa">
    </section>
</template>

<style scoped lang="scss">
.hero {
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    margin: 7rem 2rem 2rem 2rem;

    div {
        width: 35%;

        h2 {
            font-size: 3.75rem;
            font-weight: 800;
            color: #262626;
            margin-bottom: 1.5rem;

            span {
                font-size: 5rem;
                color: #E1306C;
            }
        }

        p {
            font-size: 1.25rem;
            color: #262626;
            font-weight: 500;
        }
    }

    img {
        width: 27vw;
    }
}
</style>