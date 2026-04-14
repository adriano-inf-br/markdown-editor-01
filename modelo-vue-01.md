<template>
  <section class="dashboard-card">
    <h2>{{ titulo }}</h2>
    <p>{{ descricao }}</p>
    <button @click="incrementar">Cliques: {{ contador }}</button>
  </section>
</template>

<script>
export default {
  name: 'DashboardCard',
  data() {
    return {
      titulo: 'Resumo do dia',
      descricao: 'Acompanhe os eventos em tempo real.',
      contador: 0
    };
  },
  methods: {
    incrementar() {
      this.contador += 1;
    }
  }
};
</script>

<style scoped>
.dashboard-card { padding: 1rem; border-radius: 1rem; background: #f4f6fa; }
button { margin-top: 1rem; }
</style>
