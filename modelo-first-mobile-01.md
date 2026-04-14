/* Mobile first */
.container {
  display: grid;
  gap: 1rem;
  padding: 1rem;
}

.card {
  padding: 1rem;
  border-radius: 0.75rem;
  background: #ffffff;
  box-shadow: 0 10px 24px rgba(0, 0, 0, 0.08);
}

@media (min-width: 768px) {
  .container {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

@media (min-width: 1200px) {
  .container {
    grid-template-columns: repeat(4, minmax(0, 1fr));
  }
}
