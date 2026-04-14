<template>
  <main>
    <h1>Pedidos</h1>
    <Suspense>
      <template #default>
        <PedidoLista />
      </template>
      <template #fallback>
        <p>Carregando pedidos...</p>
      </template>
    </Suspense>
  </main>
</template>

<script setup>
import PedidoLista from './PedidoLista.vue';
</script>
