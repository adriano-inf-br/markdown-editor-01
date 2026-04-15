<?php

declare(strict_types=1);

final class PedidoCalculator
{
    public function total(array $itens): float
    {
        return array_reduce($itens, function (float $soma, array $item): float {
            return $soma + ($item['quantidade'] * $item['preco_unitario']);
        }, 0.0);
    }
}

$itens = [
    ['sku' => 'TEC-01', 'quantidade' => 1, 'preco_unitario' => 349.90],
    ['sku' => 'MOU-02', 'quantidade' => 2, 'preco_unitario' => 129.90],
];

$calculator = new PedidoCalculator();
$total = $calculator->total($itens);

echo 'Total do pedido: R$ ' . number_format($total, 2, ',', '.');
