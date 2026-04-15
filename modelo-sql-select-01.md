SELECT
  numero,
  cliente_nome,
  status,
  total,
  sla_minutos
FROM pedidos
WHERE status IN ('pendente', 'separacao')
ORDER BY sla_minutos ASC, criado_em DESC
LIMIT 20;
