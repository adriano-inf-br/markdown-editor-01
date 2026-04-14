<template>
  <form class="filtro" @submit.prevent="buscar">
    <input v-model="termo" placeholder="Buscar produto" />
    <button type="submit">Pesquisar</button>
    <ul>
      <li v-for="item in resultados" :key="item.id">{{ item.nome }}</li>
    </ul>
  </form>
</template>

<script setup>
import { computed, ref } from 'vue';

const termo = ref('');
const produtos = ref([
  { id: 1, nome: 'Monitor ultrawide' },
  { id: 2, nome: 'Mouse vertical' },
  { id: 3, nome: 'Teclado ABNT2' }
]);

const resultados = computed(() => {
  const filtro = termo.value.trim().toLowerCase();
  return produtos.value.filter((item) => item.nome.toLowerCase().includes(filtro));
});

function buscar() {
  console.log('Filtro aplicado:', termo.value);
}
</script>
