<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Painel de Pedidos</title>
</head>
<body>
  <header>
    <h1>Console Markdown Enterprise</h1>
    <p>Painel operacional para acompanhar pedidos, SLA e expedição.</p>
  </header>

  <main>
    <section aria-labelledby="resumo-dia">
      <h2 id="resumo-dia">Resumo do dia</h2>
      <div class="kpis">
        <article data-status="pendente">
          <strong>12</strong>
          <span>Pedidos pendentes</span>
        </article>
        <article data-status="separacao">
          <strong>5</strong>
          <span>Em separação</span>
        </article>
        <article data-status="enviado">
          <strong>21</strong>
          <span>Enviados</span>
        </article>
      </div>
    </section>

    <section aria-labelledby="ultimos-pedidos">
      <h2 id="ultimos-pedidos">Ultimos pedidos</h2>
      <table>
        <thead>
          <tr>
            <th>Numero</th>
            <th>Cliente</th>
            <th>Status</th>
            <th>Total</th>
            <th>SLA</th>
          </tr>
        </thead>
        <tbody>
          <tr data-pedido="PED-1024">
            <td>PED-1024</td>
            <td>Ana Costa</td>
            <td>Separacao</td>
            <td>R$ 349,90</td>
            <td>2h</td>
          </tr>
          <tr data-pedido="PED-1025">
            <td>PED-1025</td>
            <td>Bruno Lima</td>
            <td>Pendente</td>
            <td>R$ 129,90</td>
            <td>45min</td>
          </tr>
        </tbody>
      </table>
    </section>
  </main>
</body>
</html>
