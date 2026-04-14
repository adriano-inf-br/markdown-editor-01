const pedidos = [
  { numero: 1024, cliente: 'Ana Costa', status: 'separacao', total: 349.9 },
  { numero: 1025, cliente: 'Bruno Lima', status: 'pendente', total: 129.9 },
  { numero: 1026, cliente: 'Carla Souza', status: 'enviado', total: 599.0 }
];

const pendentes = pedidos.filter((pedido) => pedido.status === 'pendente').length;
const faturamento = pedidos.reduce((soma, pedido) => soma + pedido.total, 0);
const resumo = pedidos
  .map((pedido) => `#${pedido.numero} - ${pedido.cliente} - ${pedido.status}`)
  .join('\n');

console.log(resumo);
console.log(`Pedidos pendentes: ${pendentes}`);
console.log(`Faturamento parcial: R$ ${faturamento.toFixed(2)}`);
