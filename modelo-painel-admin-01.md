<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Painel Admin</title>
  <style>
    body { margin: 0; font-family: Arial, sans-serif; background: #f3f4f6; }
    .layout { display: grid; grid-template-columns: 240px 1fr; min-height: 100vh; }
    .sidebar { background: #111827; color: #fff; padding: 1.5rem; }
    .content { padding: 2rem; }
    .card { background: #fff; border-radius: 1rem; padding: 1.25rem; box-shadow: 0 12px 24px rgba(0,0,0,.08); }
  </style>
</head>
<body>
  <div class="layout">
    <aside class="sidebar">
      <h1>Admin</h1>
      <p>Visao consolidada do sistema</p>
    </aside>
    <main class="content">
      <section class="card">
        <h2>Indicadores</h2>
        <p>Usuarios ativos: 1.248</p>
      </section>
    </main>
  </div>
</body>
</html>
