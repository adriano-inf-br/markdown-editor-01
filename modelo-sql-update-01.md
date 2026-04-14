UPDATE produtos
SET preco = preco * 1.08,
    atualizado_em = CURRENT_TIMESTAMP
WHERE categoria = 'perifericos';
