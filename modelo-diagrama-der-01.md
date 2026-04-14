erDiagram
    CLIENTES ||--o{ PEDIDOS : realiza
    PEDIDOS ||--|{ ITENS_PEDIDO : contem
    PRODUTOS ||--o{ ITENS_PEDIDO : compoe
    CATEGORIAS ||--o{ PRODUTOS : organiza

    CLIENTES {
      int id
      string nome
      string email
    }

    PEDIDOS {
      int id
      date criado_em
      decimal total
    }

    PRODUTOS {
      int id
      string nome
      decimal preco
    }
