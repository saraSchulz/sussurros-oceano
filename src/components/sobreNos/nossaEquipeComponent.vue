<script setup>
import { ref } from "vue";

const membroSelecionado = ref(null);

const membros = [
  {
    nome: "Lucidrey Bonilla",
    email: "lucidreymaitab.ifc@gmail.com",
    turma: "2info2",
    github: "Lucidrey",
  },
  {
    nome: "Heloisa Pereira",
    email: "Heloisapereira1402@gmail.com",
    turma: "1agro3",
  },
  {
    nome: "Roberta Ribeiro",
    email: "robertaapbeta2212@gmail.com",
    turma: "2info2",
    github: "roberta2212",
  },
  {
    nome: "Sara Schulz",
    email: "Sara.ifc2024@gamil.com",
    turma: "2info2",
    github: "saraschulz",
  },
  {
    nome: "Vitor Verplotz",
    email: "vitoremanuelsilvaverplotz2007@gmail.com",
    turma: "2info2",
    github: "vitorgil8",
  },
];

function selecionarMembro(membro) {
  membroSelecionado.value = membro;
}

function voltar() {
  membroSelecionado.value = null;
}
</script>

<template>
  <section class="nossoEquipe">
    <div class="titulo">
      <h2>Nossa Equipe</h2>
    </div>

    <div class="equipe">
      <!-- Lista de membros -->
      <div class="lista" :class="{ ativo: membroSelecionado }">
        <h3>Membros:</h3>
        <ul>
          <li v-for="m in membros" :key="m.nome" @click="selecionarMembro(m)">
            {{ m.nome }}
          </li>
        </ul>
      </div>

      <!-- Detalhes -->
      <div class="detalhes" v-if="membroSelecionado">
        <button @click="voltar">← Voltar</button>
        <h3>{{ membroSelecionado.nome }}</h3>
        <p><b>Email:</b> {{ membroSelecionado.email }}</p>
        <p><b>Turma:</b> {{ membroSelecionado.turma }}</p>
        <p v-if="membroSelecionado.github">
          <b>Github:</b> {{ membroSelecionado.github }}
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.nossoEquipe {
  width: 100%;
  align-items: center;

  & .titulo {
    margin: 2vw 0;
    display: flex;
    justify-content: center;
    font-size: 50px;

    & h2 {
      color: #000000;
      text-shadow: 0 4px 7px rgba(0, 0, 0, 0.8);
    }
  }

  & .equipe {
    min-height: 90vh;
    width: 100%;
    background: url("/public/fundo.png") no-repeat center center/cover;
    box-shadow: 0 0 75px rgba(0, 0, 0, 0.8);
    display: flex;
    align-items: center;
    gap: 5vw;
    overflow: hidden;

    & .lista {
      flex: 1;
      transition: transform 2s ease;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

      & h3 {
        font-size: 50px;
        color: #000000;
      }

      & ul {
        & li {
          color: #000000;
          font-size: 30px;
          margin: 15px;
          text-align: center;
          cursor: pointer;
          padding: 5px 10px;
          border-radius: 20px;
        }
        & li.hover{
          background-color: #90E0EF;
          padding: 5px 10px;
          border-radius: 20px;
        }
      }
    }

    & .lista.ativo {
      transform: translateX(0%);
    }

    & .detalhes {
      flex: 1;
      opacity: 1 ;
      transition: opacity 0.5s ease;

      & button {
        background-color: transparent;
        border: none;
        font-size: 20px;
        cursor: pointer;
        margin-bottom: 20px;
      }

      & h3 {
        font-size: 30px;
        color: #000000;
        margin-bottom: 20px;
      }
      & p{
        color: #000;
      }
    }
  }
}
</style>
