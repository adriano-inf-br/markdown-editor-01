SELECT
  id,
  nome,
  preco,
  estoque
FROM produtos
WHERE estoque > 0
ORDER BY preco DESC;
