SELECT
  p.numero,
  p.cliente_nome,
  p.status,
  p.sla_minutos,
  t.nome AS transportadora,
  t.prazo_dias
FROM pedidos p
INNER JOIN transportadoras t ON t.id = p.transportadora_id
WHERE p.status = 'separacao'
ORDER BY p.sla_minutos ASC, p.criado_em DESC;

-- Consulta usada para priorizar pedidos em separacao por urgencia.
