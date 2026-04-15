<?php

$quantidade = 2;
$precoUnitario = 129.90;
$total = $quantidade * $precoUnitario;

echo 'Total do pedido: R$ ' . number_format($total, 2, ',', '.');
