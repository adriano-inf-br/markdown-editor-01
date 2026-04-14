classDiagram
    class Cliente {
      +int id
      +string nome
      +string email
      +autenticar()
    }

    class Pedido {
      +int id
      +decimal total
      +calcularTotal()
    }

    class ItemPedido {
      +int quantidade
      +decimal precoUnitario
    }

    Cliente "1" --> "0..*" Pedido
    Pedido "1" --> "1..*" ItemPedido
