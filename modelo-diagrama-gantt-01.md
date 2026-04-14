gantt
    title Cronograma de Implantacao
    dateFormat  YYYY-MM-DD
    section Planejamento
    Levantamento de requisitos :done, des1, 2026-04-01, 3d
    Prototipo navegavel        :done, des2, after des1, 4d
    section Desenvolvimento
    Backend API                :active, dev1, 2026-04-08, 6d
    Frontend painel            :dev2, after dev1, 5d
    section Entrega
    Testes integrados          :test1, after dev2, 3d
    Go-live                    :milestone, go1, after test1, 1d
