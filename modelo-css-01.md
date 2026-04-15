:root {
  --surface: #ffffff;
  --page: #f4f6fa;
  --line: #e5e7eb;
  --text: #183153;
  --success: #16c79a;
  --warning: #ffb020;
  --danger: #ff647c;
}

.painel {
  display: grid;
  gap: 1.25rem;
  padding: 1.5rem;
  background: var(--page);
  color: var(--text);
}

.kpis {
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
}

.card-resumo {
  padding: 1.25rem;
  border-radius: 1rem;
  background: var(--surface);
  border: 1px solid var(--line);
  box-shadow: 0 16px 32px rgba(24, 49, 83, 0.08);
}

.card-resumo__valor {
  display: block;
  font-size: 2rem;
  font-weight: 800;
}

.badge-status {
  display: inline-flex;
  align-items: center;
  border-radius: 999px;
  padding: 0.25rem 0.75rem;
  font-size: 0.85rem;
  font-weight: 700;
}

.badge-status--pendente { background: rgba(255, 176, 32, 0.16); color: #8a5b00; }
.badge-status--separacao { background: rgba(24, 49, 83, 0.12); color: #183153; }
.badge-status--enviado { background: rgba(22, 199, 154, 0.16); color: #0f6d55; }
