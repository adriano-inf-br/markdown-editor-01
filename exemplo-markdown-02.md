




```mermaid
graph TD
    Table[Tabela Produtos] --> PK[ID: Primary Index]
    Table --> IDX_ESTOQUE[quantidade, estoque_minimo: Composite Index]
    Table --> IDX_PRECO[preco_venda: Simple Index]
    
    Note right of IDX_ESTOQUE: Acelera o filtro de 'Baixo Estoque'
```



```mermaid
quadrantChart
    title Análise de Mercado - App X
    x-axis Baixo Custo --> Alto Custo
    y-axis Baixa Inovação --> Alta Inovação
    quadrant-1 Oportunidade: Nicho Premium
    quadrant-2 Estrela: Líder de Mercado
    quadrant-3 Risco: Commoditização
    quadrant-4 Sobrevivência: Guerra de Preços
    "Nosso App": [0.7, 0.8]
    "Concorrente A": [0.3, 0.2]
```

```mermaid
import base64
import io, requests
from IPython.display import Image, display
from PIL import Image as im
import matplotlib.pyplot as plt

def mm(graph):
    graphbytes = graph.encode("utf8")
    base64_bytes = base64.urlsafe_b64encode(graphbytes)
    base64_string = base64_bytes.decode("ascii")
    img = im.open(io.BytesIO(requests.get('https://mermaid.ink/img/' + base64_string).content))
    plt.imshow(img)
    plt.axis('off') # allow to hide axis
    plt.savefig('image.png', dpi=1200)

mm("""
graph LR;
    A--> B & C & D
    B--> A & E
    C--> A & E
    D--> A & E
    E--> B & C & D
""")
```


```mermaid
block
columns 1
  db(("DB"))
  blockArrowId6<["&nbsp;&nbsp;&nbsp;"]>(down)
  block:ID
    A
    B["A wide one in the middle"]
    C
  end
  space
  D
  ID --> D
  C --> D
  style B fill:#969,stroke:#333,stroke-width:4px
```


```mermaid
timeline
    title History of Social Media Platform
    2002 : LinkedIn
    2004 : Facebook
         : Google
    2005 : YouTube
    2006 : Twitter
```

```mermaid
zenuml
    title Demo
    Alice->John: Hello John, how are you?
    John->Alice: Great!
    Alice->John: See you later!
```


```mermaid
---
config:
  sankey:
    showValues: false
---
sankey

Agricultural 'waste',Bio-conversion,124.729
Bio-conversion,Liquid,0.597
Bio-conversion,Losses,26.862
Bio-conversion,Solid,280.322
Bio-conversion,Gas,81.144
Biofuel imports,Liquid,35
Biomass imports,Solid,35
Coal imports,Coal,11.606
Coal reserves,Coal,63.965
Coal,Solid,75.571
District heating,Industry,10.639
District heating,Heating and cooling - commercial,22.505
District heating,Heating and cooling - homes,46.184
Electricity grid,Over generation / exports,104.453
Electricity grid,Heating and cooling - homes,113.726
Electricity grid,H2 conversion,27.14
Electricity grid,Industry,342.165
Electricity grid,Road transport,37.797
Electricity grid,Agriculture,4.412
Electricity grid,Heating and cooling - commercial,40.858
Electricity grid,Losses,56.691
Electricity grid,Rail transport,7.863
Electricity grid,Lighting & appliances - commercial,90.008
Electricity grid,Lighting & appliances - homes,93.494
Gas imports,Ngas,40.719
Gas reserves,Ngas,82.233
Gas,Heating and cooling - commercial,0.129
Gas,Losses,1.401
Gas,Thermal generation,151.891
Gas,Agriculture,2.096
Gas,Industry,48.58
Geothermal,Electricity grid,7.013
H2 conversion,H2,20.897
H2 conversion,Losses,6.242
H2,Road transport,20.897
Hydro,Electricity grid,6.995
Liquid,Industry,121.066
Liquid,International shipping,128.69
Liquid,Road transport,135.835
Liquid,Domestic aviation,14.458
Liquid,International aviation,206.267
Liquid,Agriculture,3.64
Liquid,National navigation,33.218
Liquid,Rail transport,4.413
Marine algae,Bio-conversion,4.375
Ngas,Gas,122.952
Nuclear,Thermal generation,839.978
Oil imports,Oil,504.287
Oil reserves,Oil,107.703
Oil,Liquid,611.99
Other waste,Solid,56.587
Other waste,Bio-conversion,77.81
Pumped heat,Heating and cooling - homes,193.026
Pumped heat,Heating and cooling - commercial,70.672
Solar PV,Electricity grid,59.901
Solar Thermal,Heating and cooling - homes,19.263
Solar,Solar Thermal,19.263
Solar,Solar PV,59.901
Solid,Agriculture,0.882
Solid,Thermal generation,400.12
Solid,Industry,46.477
Thermal generation,Electricity grid,525.531
Thermal generation,Losses,787.129
Thermal generation,District heating,79.329
Tidal,Electricity grid,9.452
UK land based bioenergy,Bio-conversion,182.01
Wave,Electricity grid,19.013
Wind,Electricity grid,289.366
```


```mermaid
xychart
    title "Sales Revenue"
    x-axis [jan, feb, mar, apr, may, jun, jul, aug, sep, oct, nov, dec]
    y-axis "Revenue (in $)" 4000 --> 11000
    bar [5000, 6000, 7500, 8200, 9500, 10500, 11000, 10200, 9200, 8500, 7000, 6000]
    line [5000, 6000, 7500, 8200, 9500, 10500, 11000, 10200, 9200, 8500, 7000, 6000]
```


```mermaid
block
columns 1
  db(("DB"))
  blockArrowId6<["&nbsp;&nbsp;&nbsp;"]>(down)
  block:ID
    A
    B["A wide one in the middle"]
    C
  end
  space
  D
  ID --> D
  C --> D
  style B fill:#969,stroke:#333,stroke-width:4px
```



```mermaid
---
title: "TCP Packet"
---
packet
0-15: "Source Port"
16-31: "Destination Port"
32-63: "Sequence Number"
64-95: "Acknowledgment Number"
96-99: "Data Offset"
100-105: "Reserved"
106: "URG"
107: "ACK"
108: "PSH"
109: "RST"
110: "SYN"
111: "FIN"
112-127: "Window"
128-143: "Checksum"
144-159: "Urgent Pointer"
160-191: "(Options and Padding)"
192-255: "Data (variable length)"
```




```mermaid
---
config:
  kanban:
    ticketBaseUrl: 'https://mermaidchart.atlassian.net/browse/#TICKET#'
---
kanban
  Todo
    [Create Documentation]
    docs[Create Blog about the new diagram]
  [In progress]
    id6[Create renderer so that it works in all cases. We also add some extra text here for testing purposes. And some more just for the extra flare.]
  id9[Ready for deploy]
    id8[Design grammar]@{ assigned: 'knsv' }
  id10[Ready for test]
    id4[Create parsing tests]@{ ticket: MC-2038, assigned: 'K.Sveidqvist', priority: 'High' }
    id66[last item]@{ priority: 'Very Low', assigned: 'knsv' }
  id11[Done]
    id5[define getData]
    id2[Title of diagram is more than 100 chars when user duplicates diagram with 100 char]@{ ticket: MC-2036, priority: 'Very High'}
    id3[Update DB function]@{ ticket: MC-2037, assigned: knsv, priority: 'High' }

  id12[Can't reproduce]
    id3[Weird flickering in Firefox]
```



```mermaid
architecture-beta
    group api(cloud)[API]

    service db(database)[Database] in api
    service disk1(disk)[Storage] in api
    service disk2(disk)[Storage] in api
    service server(server)[Server] in api

    db:L -- R:server
    disk1:T -- B:server
    disk2:T -- B:db
```


```mermaid
---
title: "Grades"
---
radar-beta
  axis m["Math"], s["Science"], e["English"]
  axis h["History"], g["Geography"], a["Art"]
  curve a["Alice"]{85, 90, 80, 70, 75, 90}
  curve b["Bob"]{70, 75, 85, 80, 90, 85}

  max 100
  min 0
```



```mermaid
treemap-beta
"Products"
    "Electronics"
        "Phones": 50
        "Computers": 30
        "Accessories": 20
    "Clothing"
        "Men's": 40
        "Women's": 40

```



```mermaid
venn-beta
  title "Team overlap"
  set Frontend
  set Backend
  union Frontend,Backend["APIs"]
```




```mermaid
venn-beta
  set A["Frontend"]
    text A1["React"]
    text A2["Design Systems"]
  set B["Backend"]
    text B1["API"]
  union A,B["Shared"]
    text AB1["OpenAPI"]
```



```mermaid
ishikawa-beta
    Blurry Photo
    Process
        Out of focus
        Shutter speed too slow
        Protective film not removed
        Beautification filter applied
    User
        Shaky hands
    Equipment
        LENS
            Inappropriate lens
            Damaged lens
            Dirty lens
        SENSOR
            Damaged sensor
            Dirty sensor
    Environment
        Subject moved too quickly
        Too dark
```



```mermaid
treeView-beta
    "packages"
        "mermaid"
            "src"
        "parser"

```


```mermaid
---
config:
    treeView:
        rowIndent: 80
        lineThickness: 3
    themeVariables:
        treeView:
            labelFontSize: '20px'
            labelColor: '#FF0000'
            lineColor: '#00FF00'
---
treeView-beta
    "packages"
        "mermaid"
            "src"
        "parser"
```


```mermaid
block-beta
  columns 4
  header: "Dashboard Financeiro (1440px)"
  
  side["Menu Lateral:<br/>• Home<br/>• Vendas<br/>• Usuários<br/>• Ajustes"]:1
  
  block:main:3
    columns 3
    nav["Barra de Busca / Notificações / Perfil"]:3
    
    card1["KPI: Vendas Totais<br/>R$ 45.000"]:1
    card2["KPI: Novos Leads<br/>120"]:1
    card3["KPI: Taxa de Conv.<br/>12%"]:1
    
    chart["Gráfico de Performance (Linha)"]:3
    table["Lista de Transações Recentes"]:3
  end
block-beta
  columns 4
  header: "Dashboard Financeiro (1440px)"
  
  side["Menu Lateral:<br/>• Home<br/>• Vendas<br/>• Usuários<br/>• Ajustes"]:1
  
  block:main:3
    columns 3
    nav["Barra de Busca / Notificações / Perfil"]:3
    
    card1["KPI: Vendas Totais<br/>R$ 45.000"]:1
    card2["KPI: Novos Leads<br/>120"]:1
    card3["KPI: Taxa de Conv.<br/>12%"]:1
    
    chart["Gráfico de Performance (Linha)"]:3
    table["Lista de Transações Recentes"]:3
  end
```


```mermaid
graph TD
    Header[Header: Logo | Links | CTA]
    Hero[Hero: Título de Impacto + Imagem + Botão]
    SocialProof[Logos: Empresas que confiam em nós]
    Features[Grid: 3 Colunas de Funcionalidades]
    Testimonials[Slider: Depoimentos de Clientes]
    Pricing[Cards: Planos Mensal / Anual]
    Footer[Footer: Sitemap | Redes Sociais]

    Header --> Hero --> SocialProof --> Features --> Testimonials --> Pricing --> Footer
```


```mermaid
kanban
  Todo
    [Visão do Produto]
    [Product Roadmap]
    [Item do Backlog A]
  Em Progresso
    [Item do Backlog B]
  Em Teste (QA)
    [Item do Backlog C]
  Concluído (Done)
    [Incremento do Produto]
    [Meta da Sprint batida]
```





```mermaid
kanban
  Todo
    Tarefa 1
    Tarefa 2
  In Progress
    Tarefa 3
  Done
    Tarefa 4
```







```mermaid
kanban
  A Fazer
    [Alta] Revisar contrato
    [Média] Atualizar documentação
  Em Execução
    [Urgente] Corrigir bug de login
  Concluído
    Configurar servidor
    Reunião de kickoff
```



```mermaid
kanban
  Backlog
    Task: Integrar API de Pagamento
    Task: Criar tela de perfil
  Em Desenvolvimento
    Task: Refatorar banco de dados
  Testando / QA
    Task: Validar responsividade
  Finalizado
    Task: Login com Google
    Task: Setup do projeto
```


Dica: Nem todos os editores de Markdown suportam nativamente o tipo kanban ainda (ele é recente no Mermaid). Se o seu editor não mostrar as colunas, você pode usar um Estado (State Diagram) ou um Fluxograma como alternativa.







```mermaid
flowchart TD
    subgraph Backlog
        b1[Planejar Sprint]
    end

    subgraph InProgress [Em Execução]
        p1[Desenvolver API]
        p2[Criar UI]
    end

    subgraph Review [Revisão]
        r1[Code Review]
    end

    %% Estilização
    style Backlog fill:#f9f,stroke:#333,stroke-width:2px
    style InProgress fill:#bbf,stroke:#333,stroke-width:2px
    style Review fill:#bfb,stroke:#333,stroke-width:2px
    style p1 fill:#ff9,color:#000 %% Destaque para um card específico
```






```mermaid
graph LR
    M1[Matéria Prima] -->|Entrada de Dados| P[Processamento/Montagem]
    P -->|Validação de Qualidade| M2[Produto Final]
    
    style P stroke-dasharray: 5 5
    Note over P: Metáfora: Nosso Motor de Cálculo <br/> funciona como uma prensa industrial.
```







```mermaid
quadrantChart
    title Registro de Partes Interessadas - Poder/Interesse
    x-axis Baixo Interesse --> Alto Interesse
    y-axis Baixo Poder --> Alto Poder
    quadrant-1 Monitorar (Baixo P/B I)
    quadrant-2 Manter Satisfeito (Alto P/B I)
    quadrant-3 Acompanhar (Baixo P/B I)
    quadrant-4 Gerenciar de Perto (Alto P/B I)
    "Equipe Interna": [0.3, 0.2]
    "Sponsor": [0.8, 0.9]
    "Cliente": [0.7, 0.8]
    "Fornecedor A": [0.2, 0.7]
    "Usuário Final": [0.1, 0.1]
```






```mermaid
board
    kanban
        A fazer
            [Definir Requisitos]
            [Estilo CSS]
        Em progresso
            [API Login]
        Feito
            [Configurar Servidor]
```






```mermaid
ishikawa
    title Causa Raiz - Atraso na Entrega
    Material: "Servidor lento"
    Material: "API Indisponível"
    Método: "Sem testes automatizados"
    Método: "Reuniões excessivas"
    Mão de Obra: "Falta de Devs"
    Mão de Obra: "Sickness"
    Máquina: "Notebooks antigos"
    Medida: "Estimativas erradas"
```






```mermaid
graph TD
    subgraph RACI
        direction TB
        M[Matriz de Responsabilidade]
        RACI_Table[

        | Tarefa | PM | Dev | QA |
        | :--- | :---: | :---: | :---: |
        | Escopo | A | C | I |
        | Codar | I | R | C |
        | Testar | I | C | R |
        ]
    end
```





```mermaid
kanban
  Todo
    Definir requisitos
    Criar banco de dados
  In Progress
    Desenvolver API
  Done
    Setup do servidor
```





```mermaid
quadrantChart
    title Matriz de Riscos (Impacto x Probabilidade)
    x-axis Baixa Probabilidade --> Alta Probabilidade
    y-axis Baixo Impacto --> Alto Impacto
    quadrant-1 Monitorar
    quadrant-2 Mitigar Urgente
    quadrant-3 Ignorar
    quadrant-4 Planejar Contingência
    Risco A: [0.3, 0.4]
    Risco B: [0.8, 0.9]
    Risco C: [0.7, 0.2]
```


O Mermaid é excelente porque o diagrama vira código. Se o escopo mudar, você altera uma linha de texto e o gráfico se ajusta sozinho, mantendo a documentação sempre "viva" e versionada.






```mermaid
gantt
    title Roadmap de User Stories - Sprint 1
    dateFormat  YYYY-MM-DD
    section Checkout
    Story: Autenticação Social    :active,  st1, 2023-10-01, 3d
    Story: Integração PayPal      :         st2, after st1, 5d
    section Perfil
    Story: Upload de Avatar       :         st3, 2023-10-02, 4d
```



Melhores Práticas
Mantenha Simples: Diagramas muito complexos são difíceis de entender
Use Cores com Propósito: Destaque elementos importantes
Seja Consistente: Use o mesmo estilo em toda documentação
Versione seus Diagramas: Guarde o código Mermaid, não apenas as imagens
Documente o Contexto: Adicione descrições ao redor dos diagramas






