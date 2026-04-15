<template>
  <section class="card-pedido">
    <header class="card-pedido__header">
      <h2>{{ pedido.numero }}</h2>
      <span :class="['badge-status', `badge-status--${pedido.status}`]">{{ pedido.status }}</span>
    </header>

    <p>Cliente: {{ pedido.cliente }}</p>
    <p>Total: {{ totalFormatado }}</p>

    <button @click="marcarComoEnviado" :disabled="pedido.status === 'enviado'">
      Marcar como enviado
    </button>
  </section>
</template>

<script>
export default {
  name: 'CardPedido',
  data() {
    return {
      pedido: {
        numero: 'PED-1024',
        cliente: 'Ana Costa',
        status: 'separacao',
        total: 349.9
      }
    };
  },
  computed: {
    totalFormatado() {
      return new Intl.NumberFormat('pt-BR', { style: 'currency', currency: 'BRL' }).format(this.pedido.total);
    }
  },
  methods: {
    marcarComoEnviado() {
      this.pedido.status = 'enviado';
      this.$emit('status-atualizado', this.pedido);
    }
  }
};
</script>

<style scoped>
.card-pedido { padding: 1rem; border-radius: 1rem; background: #f4f6fa; }
.card-pedido__header { display: flex; justify-content: space-between; align-items: center; gap: 1rem; }
.badge-status { padding: 0.2rem 0.6rem; border-radius: 999px; background: #dbeafe; }
button { margin-top: 1rem; }
</style>
