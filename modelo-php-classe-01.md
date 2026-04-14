<?php

final class Cliente
{
    public function __construct(
        private string $nome,
        private string $email
    ) {
    }

    public function saudacao(): string
    {
        return sprintf('Olá, %s! Seu contato é %s.', $this->nome, $this->email);
    }
}

$cliente = new Cliente('Marina', 'marina@empresa.com');
echo $cliente->saudacao();
