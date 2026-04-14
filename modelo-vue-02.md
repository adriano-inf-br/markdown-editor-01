<template>
  <form class="filtro-pedidos" @submit.prevent>
    <input v-model="termo" placeholder="Buscar por cliente" />
    <ul>
      <li v-for="pedido in filtrados" :key="pedido.numero">
        #{{ pedido.numero }} - {{ pedido.cliente }}
      </li>
    </ul>
  </form>
</template>

<script setup>
import { computed, ref } from 'vue';

const termo = ref('');
const pedidos = ref([
  { numero: 1024, cliente: 'Ana Costa' },
  { numero: 1025, cliente: 'Bruno Lima' },
  { numero: 1026, cliente: 'Carla Souza' }
]);

const filtrados = computed(() => {
  const filtro = termo.value.trim().toLowerCase();
  return pedidos.value.filter((pedido) => pedido.cliente.toLowerCase().includes(filtro));
});
</script>
