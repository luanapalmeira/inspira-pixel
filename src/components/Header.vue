<script setup>
import { Icon } from "@iconify/vue";
</script>

<template>
  <header>
    <img src="../assets/logo.svg" alt="Logo" />

    <nav>
      <ul>
        <li>
          <a href="">
            <Icon class="icone-1" icon="iconamoon:search-thin" />
          </a>
        </li>
        <li><a href="">Início</a></li>
        <li><a href="">Galeria</a></li>
        <li><a href="">Favoritos</a></li>
        <li>
          <a href="">
            <Icon class="icone-2" icon="octicon:person-24" />
          </a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style scoped lang="scss">
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 2rem;

    ul {
      display: flex;
      list-style: none;
      gap: 3rem;
      align-items: center;
      justify-content: center;

      a {
        text-decoration: none;
        color: #262626;
        font-size: 1.5rem;
        font-weight: 400;

        &:hover {
          text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        .icone-1 {
          font-size: 2rem;  //Esses ícones estão sendo tratados como texto
        }

        .icone-2 {
          font-size: 2rem;
          color: #E1306C;
        }
      }
    }
  }
</style>
