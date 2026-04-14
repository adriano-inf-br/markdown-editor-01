const produtos = [
  { id: 1, nome: 'Notebook', preco: 4599.9 },
  { id: 2, nome: 'Mouse sem fio', preco: 129.9 },
  { id: 3, nome: 'Monitor 27', preco: 1499.0 }
];

const total = produtos.reduce((soma, item) => soma + item.preco, 0);
const resumo = produtos
  .map((item) => `${item.nome}: R$ ${item.preco.toFixed(2)}`)
  .join('\n');

console.log(resumo);
console.log(`Total do carrinho: R$ ${total.toFixed(2)}`);
