<template>
  <form class="filtro-pedidos" @submit.prevent>
    <input v-model="termo" placeholder="Buscar por cliente ou numero" />

    <ul>
      <li v-for="pedido in filtrados" :key="pedido.numero">
        <strong>{{ pedido.numero }}</strong> - {{ pedido.cliente }}
        <small>({{ pedido.status }})</small>
      </li>
    </ul>
  </form>
</template>

<script setup>
import { computed, ref } from 'vue';

const termo = ref('');
const pedidos = ref([
  { numero: 'PED-1024', cliente: 'Ana Costa', status: 'separacao' },
  { numero: 'PED-1025', cliente: 'Bruno Lima', status: 'pendente' },
  { numero: 'PED-1026', cliente: 'Carla Souza', status: 'enviado' }
]);

const filtrados = computed(() => {
  const filtro = termo.value.trim().toLowerCase();
  return pedidos.value.filter((pedido) => {
    return [pedido.numero, pedido.cliente, pedido.status].some((campo) => campo.toLowerCase().includes(filtro));
  });
});
</script>
