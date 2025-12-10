<script setup>
import { Icon } from "@iconify/vue";
import { ref } from "vue";

const menuAtivo = ref(false);

const toggleMenu = () => {
  menuAtivo.value = !menuAtivo.value;
};
</script>

<template>
  <header>
    <img src="../assets/logo.svg" alt="Logo" />

    <nav :class="['menu', { mostrar: menuAtivo }]">
      <ul>
        <li>
          <a href="">
            <Icon class="icone-1" icon="iconamoon:search-thin" />
          </a>
        </li>
        <li><a href="#" target="_blank">Início</a></li>
        <li><a href="#" target="_blank">Galeria</a></li>
        <li><a href="#" target="_blank">Favoritos</a></li>
        <li>
          <a href="">
            <Icon class="icone-2" icon="octicon:person-24" />
          </a>
        </li>
      </ul>
    </nav>

    <div class="backdrop" :class="{ ativo: menuAtivo }" @click="toggleMenu"></div>

    <button class="botao_menu" @click="toggleMenu">
      <Icon icon="pepicons-pencil:menu" width="20" height="20" />
    </button>
  </header>
</template>

<style scoped lang="scss">
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 2rem;

  .botao_menu {
    display: none; // aparece só no mobile
    background: none;
    border: none;
    cursor: pointer;

    svg {
      width: 30px;
      height: 30px;
    }
  }

  nav.menu {
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
          font-size: 2rem;  //Esse icones estão sendo tratados como texto
        }

        .icone-2 {
          font-size: 2rem;
          color: #e1306c;
        }
      }
    }
  }
}

.backdrop {
  position: fixed;
  inset: 0;
  background: rgba(0, 0, 0, 0);
  pointer-events: none;
  transition: background 0.3s ease;
  z-index: 997;
}

.backdrop.ativo {
  background: rgba(0, 0, 0, 0.5);
  pointer-events: all;
}

@media (max-width: 768px) {
  header {
    position: relative;
    margin: 1rem;

    /* Menu hambúrguer aparece */
    .botao_menu {
      display: block;
      z-index: 999;
    }

    /* Nav fechado */
    nav.menu {
      position: relative;
      background: transparent;
      width: auto;
      padding: 0;

      ul {
        display: flex;
        flex-direction: row;
        gap: 1rem;
        align-items: center;
        margin: 0;
        padding: 0;

        /* Somente o ícone de busca aparece */
        li {
          &:not(:first-child) {
            display: none;
          }
        }
      }
    }

    /* Nav aberto */
    nav.menu.mostrar {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background: white;
      padding: 2rem 0;
      transition: top 0.4s ease;
      z-index: 998;

      ul {
        display: flex;
        flex-direction: column;
        gap: 2rem;

        /* Mostra todos os itens */
        li {
          display: block !important;
        }

        a {
          font-size: 1.5rem;
        }
      }
    }
  }

  /* Ícone de busca some quando o menu abre */
  nav.menu.mostrar ul li:first-child {
    display: none !important;
  }

  /* ícone de busca ao lado do hambúrguer */
  nav.menu ul li:first-child {
    position: absolute;
    right: 60px;
    top: 50%;
    transform: translateY(-50%);
    display: block !important;
    z-index: 999;
  }

  .botao_menu {
    position: absolute;
    right: 10px;
    top: 50%;
    transform: translateY(-50%);
  }

  /* Backdrop na frente do conteúdo */
  .backdrop {
    z-index: 997;
  }
}

/* Cor do menu */
.botao_menu svg {
  transition: color 0.3s ease;
  color: #e1306c;
}

/* Quando abre o menu, fica preto */
.menu.mostrar + .backdrop + .botao_menu svg {
  color: #262626;
}
</style>
