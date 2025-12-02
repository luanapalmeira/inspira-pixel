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
            <Icon class="icone-1" icon="material-symbols:search" />
          </a>
        </li>
        <li><a href="">inicio</a></li>
        <li><a href="">Galeria</a></li>
        <li><a href="">Favoritos</a></li>
        <li>
          <a href="">
            <Icon class="icone-2" icon="material-symbols:person-outline" />
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
      gap: 1rem;
      align-items: center;

      a {
        text-decoration: none;
        color: #000000;

        .icone-1 {
          font-size: 1.5rem;  //Essees ícones estão sendo tratados como texto
        }

        .icone-2 {
          font-size: 1.5rem;
          color: #E1306C;
        }
      }
    }
  }
</style>
