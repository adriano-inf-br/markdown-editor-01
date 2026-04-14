SELECT
  numero,
  cliente_nome,
  status,
  total
FROM pedidos
WHERE status IN ('pendente', 'separacao')
ORDER BY criado_em DESC;
