classDiagram
    class Pedido {
      +string numero
      +string status
      +decimal total
      +calcularPrazo()
    }

    class Cliente {
      +string nome
      +string email
    }

    class Transportadora {
      +string nome
      +int prazoDias
    }

    Cliente "1" --> "0..*" Pedido
    Pedido "1" --> "1" Transportadora
