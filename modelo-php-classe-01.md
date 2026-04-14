<?php

final class Pedido
{
    public function __construct(
        private int $numero,
        private string $status,
        private float $total
    ) {
    }

    public function resumo(): string
    {
        return sprintf('Pedido #%d - %s - R$ %.2f', $this->numero, strtoupper($this->status), $this->total);
    }
}

$pedido = new Pedido(1024, 'separacao', 349.90);
echo $pedido->resumo();
