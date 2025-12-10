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

@media (max-width: 768px) {
    .hero {
        display: flex;
        flex-direction: column-reverse;
        justify-content: space-between;
        height: 60vh;
        margin-top: 3rem;

        div {
            width: 100%;
            text-align: center;

            h2 {
                font-size: 2rem;
                margin-bottom: 1rem;

                span {
                    font-size: 2.5rem;
                }
            }

            p {
                font-size: 0.8rem;
            }
        }

        img {
            width: 75vw;
        }
    }
}
</style>