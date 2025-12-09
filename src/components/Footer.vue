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

        <div>
            <h4>Assine nossa newsletter</h4>
            <input type="email" name="email" id="email" placeholder="Seu email" >
            <button>Inscrever-se</button>
        </div>
    </section>

    <div>
        <ol>
            <a href="#" target="_blank"><li id="facebook">
                <Icon icon="ic:baseline-facebook" width="24" height="24" />
            </li></a>

            <a href="#" target="_blank"><li id="linkedin">
                <Icon icon="entypo-social:linkedin-with-circle" width="24" height="24" />
            </li></a>

            <a href="#" target="_blank"><li id="instagram">
                <Icon icon="entypo-social:instagram-with-circle" width="24" height="24" />
            </li></a>

            <a href="#" target="_blank"><li id="twitter">
                <Icon icon="ant-design:twitter-circle-filled" width="24" height="24" />
            </li></a>
        </ol>
    </div>
</template>

<style scoped lang="scss"></style>