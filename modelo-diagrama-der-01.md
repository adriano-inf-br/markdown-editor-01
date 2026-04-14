erDiagram
    CLIENTES ||--o{ PEDIDOS : realiza
    PEDIDOS ||--|| TRANSPORTADORAS : utiliza
    PEDIDOS ||--|{ ITENS_PEDIDO : contem
    PRODUTOS ||--o{ ITENS_PEDIDO : compoe

    CLIENTES {
      int id
      string nome
      string email
    }

    PEDIDOS {
      int id
      string numero
      int transportadora_id
      string status
      decimal total
      datetime atualizado_em
    }

    TRANSPORTADORAS {
      int id
      string nome
      int prazo_dias
    }
