const pedidos = [
  { numero: 'PED-1024', cliente: 'Ana Costa', status: 'separacao', total: 349.9, slaMinutos: 120 },
  { numero: 'PED-1025', cliente: 'Bruno Lima', status: 'pendente', total: 129.9, slaMinutos: 45 },
  { numero: 'PED-1026', cliente: 'Carla Souza', status: 'enviado', total: 599.0, slaMinutos: 0 }
];

const formatarMoeda = (valor) => new Intl.NumberFormat('pt-BR', {
  style: 'currency',
  currency: 'BRL'
}).format(valor);

const indicadores = pedidos.reduce((acc, pedido) => {
  acc.total += pedido.total;
  acc[pedido.status] = (acc[pedido.status] || 0) + 1;
  return acc;
}, { total: 0, pendente: 0, separacao: 0, enviado: 0 });

const resumo = pedidos
  .map((pedido) => `${pedido.numero} | ${pedido.cliente} | ${pedido.status} | ${formatarMoeda(pedido.total)}`)
  .join(String.fromCharCode(10));

console.log(resumo);
console.table(indicadores);
