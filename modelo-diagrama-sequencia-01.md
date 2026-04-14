sequenceDiagram
    participant Operador
    participant Painel
    participant API
    participant Banco

    Operador->>Painel: Atualiza status do pedido
    Painel->>API: PATCH /pedidos/PED-1024
    API->>Banco: UPDATE pedidos SET status = 'enviado'
    Banco-->>API: Confirmacao
    API-->>Painel: 200 OK
    Painel-->>Operador: Timeline atualizada
