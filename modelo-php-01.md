<?php

declare(strict_types=1);

function calcularFrete(float $subtotal): float
{
    if ($subtotal >= 300) {
        return 0.0;
    }

    return 19.90;
}

$subtotal = 249.90;
$frete = calcularFrete($subtotal);

echo 'Subtotal: R$ ' . number_format($subtotal, 2, ',', '.') . PHP_EOL;
echo 'Frete: R$ ' . number_format($frete, 2, ',', '.') . PHP_EOL;
