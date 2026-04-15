CREATE TABLE pedidos (
  id INT PRIMARY KEY AUTO_INCREMENT,
  numero VARCHAR(20) NOT NULL UNIQUE,
  cliente_nome VARCHAR(120) NOT NULL,
  transportadora_id INT NOT NULL,
  status ENUM('pendente', 'separacao', 'enviado', 'cancelado') NOT NULL DEFAULT 'pendente',
  total DECIMAL(10, 2) NOT NULL,
  sla_minutos INT NOT NULL DEFAULT 0,
  criado_em TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  atualizado_em TIMESTAMP NULL DEFAULT NULL,
  INDEX idx_pedidos_status_criado (status, criado_em),
  CONSTRAINT fk_pedidos_transportadora
    FOREIGN KEY (transportadora_id) REFERENCES transportadoras(id)
);
