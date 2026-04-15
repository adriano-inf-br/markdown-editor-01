UPDATE pedidos
SET status = 'enviado',
    atualizado_em = CURRENT_TIMESTAMP,
    sla_minutos = 0
WHERE numero = 'PED-1024'
  AND status = 'separacao';
