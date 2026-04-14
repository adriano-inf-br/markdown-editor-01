sequenceDiagram
    participant Cliente
    participant Frontend
    participant API
    participant Banco

    Cliente->>Frontend: Confirma compra
    Frontend->>API: POST /pedidos
    API->>Banco: INSERT pedido e itens
    Banco-->>API: Pedido salvo
    API-->>Frontend: 201 Created
    Frontend-->>Cliente: Exibe numero do pedido
