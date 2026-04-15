<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Painel Administrativo</title>
  <style>
    body { margin: 0; font-family: Arial, sans-serif; background: #f3f4f6; }
    .layout { display: grid; grid-template-columns: 240px 1fr; min-height: 100vh; }
    .sidebar { background: #111827; color: #fff; padding: 1.5rem; }
    .content { padding: 2rem; }
    .kpis { display: grid; gap: 1rem; grid-template-columns: repeat(3, minmax(0, 1fr)); }
    .card { background: #fff; border-radius: 1rem; padding: 1.25rem; box-shadow: 0 12px 24px rgba(0,0,0,.08); }
  </style>
</head>
<body>
  <div class="layout">
    <aside class="sidebar">
      <h1>Operacao</h1>
      <p>Pedidos, estoque e suporte</p>
    </aside>
    <main class="content">
      <section class="kpis">
        <article class="card"><strong>Pendentes</strong><p>12 pedidos</p></article>
        <article class="card"><strong>Separacao</strong><p>5 pedidos</p></article>
        <article class="card"><strong>Enviados</strong><p>21 pedidos</p></article>
      </section>
    </main>
  </div>
</body>
</html>
