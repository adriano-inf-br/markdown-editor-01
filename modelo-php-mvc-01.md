<?php

declare(strict_types=1);

final class PedidoController
{
    public function __construct(private PedidoRepository $repository)
    {
    }

    public function index(): array
    {
        return [
            'view' => 'pedidos.index',
            'data' => [
                'pedidos' => $this->repository->ultimos(limit: 10),
                'kpis' => $this->repository->resumoOperacional(),
            ],
        ];
    }
}

final class PedidoRepository
{
    public function ultimos(int $limit): array
    {
        return [
            ['numero' => 'PED-1024', 'cliente' => 'Ana Costa', 'status' => 'separacao'],
            ['numero' => 'PED-1025', 'cliente' => 'Bruno Lima', 'status' => 'pendente'],
        ];
    }

    public function resumoOperacional(): array
    {
        return ['pendentes' => 12, 'separacao' => 5, 'enviados' => 21];
    }
}
