UPDATE pedidos
SET status = 'enviado',
    atualizado_em = CURRENT_TIMESTAMP
WHERE numero = 'PED-1024';
