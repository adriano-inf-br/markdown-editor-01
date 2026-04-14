# Documento Modelo 4

## Pipeline de entrega com Mermaid e código

Exemplo enxuto para validar exportação HTML, highlight de código e renderização Mermaid na mesma página.

---

## Backend

```php
function buscarPedidos(PDO $pdo): array
{
    $stmt = $pdo->query('SELECT id, total FROM pedidos ORDER BY id DESC');
    return $stmt->fetchAll(PDO::FETCH_ASSOC);
}
```

## Frontend

```javascript
const atualizarResumo = (pedidos) => {
  const total = pedidos.reduce((soma, item) => soma + item.total, 0);
  document.querySelector('#total').textContent = total.toFixed(2);
};
```

## Fluxo

```mermaid
sequenceDiagram
    participant Usuario
    participant SPA
    participant API
    participant DB

    Usuario->>SPA: Abre dashboard
    SPA->>API: GET /pedidos/resumo
    API->>DB: Consulta totais
    DB-->>API: Dados agregados
    API-->>SPA: JSON com métricas
    SPA-->>Usuario: Atualiza cards
```
