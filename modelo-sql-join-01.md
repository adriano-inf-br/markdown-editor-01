SELECT
  p.nome AS produto,
  c.nome AS categoria,
  f.nome AS fornecedor
FROM produtos p
INNER JOIN categorias c ON c.id = p.categoria_id
LEFT JOIN fornecedores f ON f.id = p.fornecedor_id
ORDER BY p.nome;
