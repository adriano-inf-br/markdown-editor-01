<?php

class ProdutoController
{
    public function index(): array
    {
        $repository = new ProdutoRepository();
        $produtos = $repository->all();

        return [
            'view' => 'produtos.index',
            'data' => ['produtos' => $produtos]
        ];
    }
}

class ProdutoRepository
{
    public function all(): array
    {
        return [
            ['id' => 1, 'nome' => 'Teclado mecânico'],
            ['id' => 2, 'nome' => 'Headset USB']
        ];
    }
}
