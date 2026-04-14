CREATE TABLE pedidos (
  id INT PRIMARY KEY AUTO_INCREMENT,
  numero VARCHAR(20) NOT NULL UNIQUE,
  cliente_nome VARCHAR(120) NOT NULL,
  transportadora_id INT NOT NULL,
  status VARCHAR(30) NOT NULL,
  total DECIMAL(10, 2) NOT NULL,
  criado_em TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  atualizado_em TIMESTAMP NULL DEFAULT NULL,
  CONSTRAINT fk_pedidos_transportadora
    FOREIGN KEY (transportadora_id) REFERENCES transportadoras(id)
);
