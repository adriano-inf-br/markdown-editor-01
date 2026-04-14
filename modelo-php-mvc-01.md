<?php

class PedidoController
{
    public function index(): array
    {
        $repository = new PedidoRepository();

        return [
            'view' => 'pedidos.index',
            'data' => [
                'pedidos' => $repository->ultimos(10),
            ],
        ];
    }
}

class PedidoRepository
{
    public function ultimos(int $limite): array
    {
        return [
            ['numero' => 1024, 'cliente' => 'Ana Costa', 'status' => 'separacao'],
            ['numero' => 1025, 'cliente' => 'Bruno Lima', 'status' => 'pendente'],
        ];
    }
}
