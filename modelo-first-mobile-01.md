.painel-operacao {
  display: grid;
  gap: 1rem;
  padding: 1rem;
}

.card-kpi {
  padding: 1rem;
  border-radius: 0.75rem;
  background: #ffffff;
  box-shadow: 0 10px 24px rgba(15, 23, 42, 0.08);
}

.card-kpi__rotulo {
  display: block;
  margin-bottom: 0.5rem;
  color: #6b7280;
}

.card-kpi__valor {
  font-size: 1.75rem;
  font-weight: 700;
}

@media (min-width: 768px) {
  .painel-operacao {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

@media (min-width: 1200px) {
  .painel-operacao {
    grid-template-columns: repeat(4, minmax(0, 1fr));
  }
}
