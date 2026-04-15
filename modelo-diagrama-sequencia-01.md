sequenceDiagram
    autonumber
    participant Operador
    participant Painel
    participant API
    participant Banco
    participant Notificador

    Operador->>Painel: Marca PED-1024 como enviado
    Painel->>API: PATCH /pedidos/PED-1024 { status: enviado }
    API->>Banco: Atualiza status e atualizado_em
    Banco-->>API: Commit realizado
    API->>Notificador: Publica evento PedidoEnviado
    Notificador-->>Painel: Atualiza timeline e badge
    API-->>Painel: 200 OK com payload consolidado
