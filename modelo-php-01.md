<?php

declare(strict_types=1);

function calcularTotalPedido(array $itens): float
{
    $total = 0.0;

    foreach ($itens as $item) {
        $total += $item['quantidade'] * $item['preco_unitario'];
    }

    return $total;
}

$itens = [
    ['produto' => 'Teclado mecanico', 'quantidade' => 1, 'preco_unitario' => 349.90],
    ['produto' => 'Mouse sem fio', 'quantidade' => 2, 'preco_unitario' => 129.90],
];

echo 'Total do pedido: R$ ' . number_format(calcularTotalPedido($itens), 2, ',', '.');
