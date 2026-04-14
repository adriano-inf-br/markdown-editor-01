gantt
    title Operacao de implantacao do painel de pedidos
    dateFormat  YYYY-MM-DD
    section Descoberta
    Mapear fluxos atuais         :done, a1, 2026-04-01, 3d
    Definir indicadores          :done, a2, after a1, 2d
    section Entrega
    Construir dashboard          :active, b1, 2026-04-07, 5d
    Integrar status de pedidos   :b2, after b1, 4d
    section Validacao
    Testar alertas operacionais  :c1, after b2, 3d
    Publicar versao inicial      :milestone, c2, after c1, 1d
