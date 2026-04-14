<template>
  <main>
    <h1>Painel de Pedidos</h1>
    <Suspense>
      <template #default>
        <ListaPedidos />
      </template>
      <template #fallback>
        <p>Carregando operacao...</p>
      </template>
    </Suspense>
  </main>
</template>

<script setup>
import ListaPedidos from './ListaPedidos.vue';
</script>
