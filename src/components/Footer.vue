<script setup>
import { Icon } from "@iconify/vue";
</script>

<template>
    <section>
        <article>
            <h4>Contato</h4>
            <ul>
                <li><a href="#" target="_blank"> contato@inspiralens.com </a></li>
                <li><a href="#" target="_blank"> Central de ajuda </a></li>
                <li>Rio de Janeiro – Brasil</li>
            </ul>
        </article>

        <article>
            <h4>Sobre</h4>
            <ul>
                <li><a href="#" target="_blank"> Politicas </a></li>
                <li><a href="#" target="_blank"> Politicas de privacidade </a></li>
                <li><a href="#" target="_blank"> Blog </a></li>
            </ul>
        </article>

        <div class="newsletter">
            <h4>Assine nossa newsletter</h4>
            <input type="email" name="email" id="email" placeholder="Seu email">
            <button>Inscrever-se</button>
        </div>
    </section>

    <div class="redes-socias">
        <ol>
            <li>
                <a href="#" target="_blank">
                    <Icon icon="ic:baseline-facebook" />
                </a>
            </li>

            <li>
                <a href="#" target="_blank">
                    <Icon icon="entypo-social:linkedin-with-circle" />
                </a>
            </li>

            <li>
                <a href="#" target="_blank">
                    <Icon icon="entypo-social:instagram-with-circle" />
                </a>
            </li>

            <li>
                <a href="#" target="_blank">
                    <Icon icon="ant-design:twitter-circle-filled" />
                </a>
            </li>
        </ol>
    </div>
</template>

<style scoped lang="scss">
section {
    display: flex;
    flex-direction: row;
    margin-left: 15rem;
    width: 70%;
    height: 20vh;
    gap: 5rem;

    article {
        width: 18%;

        h4 {
            font-size: 1.5rem;
            font-weight: 600;
            color: #262626;
            margin-bottom: 0.5rem;
        }

        ul {
            list-style: none;
            display: flex;
            flex-direction: column;
            gap: 10px;

            a {
                font-size: 1rem;
                font-weight: 400;
                color: #000000;
                text-decoration: none;

                &:hover {
                    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
                }
            }
        }
    }

    .newsletter {
        margin-left: 20rem;
        width: 35%;
        display: flex;
        flex-direction: column;
        gap: 1rem;

        h4 {
            font-size: 1.5rem;
            font-weight: 600;
            color: #262626;
        }

        input {
            border: none;
            border-radius: 5px;
            height: 5vh;
            width: 85%;
            background-color: #E6E6E63B;
            padding-left: 1rem;

            &::placeholder {
                color: #0707077D;
                font-size: 1rem;
                font-weight: 500;
            }
        }

        button {
            height: 4vh;
            width: 32%;
            border: none;
            border-radius: 5px;
            background-color: #E1306C;
            cursor: pointer;
            font-size: 1rem;
            font-weight: 700;
            color: #FFFFFF;

            &:hover {
                filter: brightness(85%);
                transition: 0.3;
            }
        }
    }
}

.redes-socias {
    height: 10vh;
    display: flex;
    justify-content: center;
    align-items: center;

    ol {
        display: flex;
        flex-direction: row;
        list-style: none;
        gap: 1rem;

        a {
            font-size: 2rem;
            color: #262626;

            &:hover {
                color: #E1306C;
                transition: 0.3;
            }
        }
    }
}
</style>