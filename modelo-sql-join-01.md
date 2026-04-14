SELECT
  p.numero,
  p.cliente_nome,
  t.nome AS transportadora,
  t.prazo_dias
FROM pedidos p
INNER JOIN transportadoras t ON t.id = p.transportadora_id
WHERE p.status = 'separacao'
ORDER BY p.criado_em DESC;
