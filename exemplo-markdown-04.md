# Documento Modelo 4

## Pipeline do pedido ao envio

Documento enxuto para validar exportacao HTML, highlight de codigo e renderizacao Mermaid em um fluxo mais proximo de producao.

---

## Backend

```php
function atualizarStatus(PDO $pdo, string $numero, string $status): array
{
    $stmt = $pdo->prepare('UPDATE pedidos SET status = :status, atualizado_em = NOW() WHERE numero = :numero');
    $stmt->execute(['status' => $status, 'numero' => $numero]);

    return ['numero' => $numero, 'status' => $status];
}
```

## Frontend

```javascript
const aplicarAtualizacao = ({ numero, status }) => {
  const badge = document.querySelector(`[data-pedido="${numero}"] .badge-status`);
  if (badge) badge.textContent = status;
};
```

## Fluxo

```mermaid
sequenceDiagram
    autonumber
    participant Operador
    participant Painel
    participant API
    participant Banco
    participant WebSocket

    Operador->>Painel: Marca pedido como enviado
    Painel->>API: PATCH /pedidos/PED-1024
    API->>Banco: Persiste novo status
    Banco-->>API: Status salvo
    API->>WebSocket: Emite evento PedidoAtualizado
    WebSocket-->>Painel: Atualiza badge e timeline
    API-->>Operador: Confirma sucesso
```
