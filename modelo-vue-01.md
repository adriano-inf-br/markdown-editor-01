<template>
  <section class="card-pedido">
    <h2>Pedido #{{ pedido.numero }}</h2>
    <p>Cliente: {{ pedido.cliente }}</p>
    <p>Status: {{ pedido.status }}</p>
    <button @click="marcarComoEnviado">Marcar como enviado</button>
  </section>
</template>

<script>
export default {
  name: 'CardPedido',
  data() {
    return {
      pedido: {
        numero: 1024,
        cliente: 'Ana Costa',
        status: 'separacao'
      }
    };
  },
  methods: {
    marcarComoEnviado() {
      this.pedido.status = 'enviado';
    }
  }
};
</script>

<style scoped>
.card-pedido { padding: 1rem; border-radius: 1rem; background: #f4f6fa; }
button { margin-top: 1rem; }
</style>
