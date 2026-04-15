# markdown-editor-01

Editor Markdown em arquivo unico, com foco em produtividade, legibilidade e exportacao HTML pronta para uso.

O projeto combina:

- **Vue 3**
- **Mermaid**
- **Highlight.js**
- **persistencia local no navegador**
- **modelos prontos por linguagem**
- **preview com fundo claro**
- **exportacao HTML standalone**
- **layout mobile-first**
- **acessibilidade e atalhos de teclado**

---

## Recursos principais

- Editor Markdown com visualizacao em tempo real
- Renderizacao de diagramas Mermaid
- Destaque de sintaxe para varias linguagens
- Exportacao de HTML standalone com tema claro e preparado para impressao
- Persistencia local em `localStorage`
- Toolbar com insercao de modelos por linguagem
- Painel lateral recolhivel
- Preview recolhivel no mobile
- Toolbar recolhivel para ampliar a area util de edicao
- Estados de foco visivel e navegacao por teclado
- Atalhos:
  - `Ctrl+S` / `Cmd+S` para salvar
  - `Escape` para fechar painéis moveis

---

## Experiencia de interface

### Mobile-first

A interface foi desenhada para funcionar bem em telas pequenas, com:

- paineis laterais sob demanda
- preview sob demanda no mobile
- compactacao progressiva em viewports estreitos
- suporte a safe areas
- melhor uso da altura da tela em dispositivos com pouco espaco vertical

### Leitura e impressao

O editor e o preview usam **fundo branco com tipografia escura**, e a exportacao HTML segue a mesma linha visual para refletir melhor o resultado final em tela e em futuras impressoes.

### Acessibilidade

- foco visivel
- botoes semanticamente corretos
- `aria-label`, `aria-expanded`, `aria-controls`
- lista de documentos com `aria-current`
- toolbar com `role="toolbar"`
- restauracao de foco ao abrir/fechar paineis moveis

---

## Guia dos modelos

Os snippets foram organizados em **tres niveis de complexidade** para equilibrar estudo, reaproveitamento e base profissional.

### Iniciante

Modelos curtos, diretos e faceis de entender:

- `modelo-html-index-01.md`
- `modelo-php-01.md`
- `modelo-php-ansi-01.md`
- `modelo-ruby-01.md`
- `modelo-pascal-01.md`
- `modelo-c-ansi-01.md`
- `modelo-c-plus-01.md`
- `modelo-sql-select-01.md`
- `modelo-sql-insert-01.md`
- `modelo-sql-delete-01.md`
- `modelo-diagrama-kamban-01.md`
- `modelo-grafico-pizza-01.md`
- `exemplo-markdown-03.md`

### Intermediario

Modelos com estrutura mais pratica e reutilizavel:

- `modelo-html-01.md`
- `modelo-css-01.md`
- `modelo-first-mobile-01.md`
- `modelo-painel-admin-01.md`
- `modelo-js-01.md`
- `modelo-php-classe-01.md`
- `modelo-vue-01.md`
- `modelo-vue-02.md`
- `modelo-c-sharp-01.md`
- `modelo-sql-update-01.md`
- `modelo-diagrama-classes-01.md`
- `modelo-diagrama-gantt-01.md`
- `modelo-prompt-ia-01.md`

### Avancado

Modelos mais proximos de producao, com fluxo, modelagem e integracao mais ricos:

- `modelo-php-mvc-01.md`
- `modelo-vue-03.md`
- `modelo-sql-create-01.md`
- `modelo-sql-join-01.md`
- `modelo-diagrama-sequencia-01.md`
- `modelo-diagrama-der-01.md`
- `exemplo-markdown-04.md`

### Arquivos auxiliares

Arquivos que permanecem no repositório como apoio documental ou catalogo complementar:

- `README.md`
- `exemplo-markdown-01.md`
- `exemplo-markdown-02.md`
- `x copy.md`

---

## Como usar

1. Abra `index.html` no navegador
2. Crie um novo documento ou selecione um existente
3. Use a toolbar para inserir modelos prontos
4. Edite o Markdown no painel principal
5. Abra o preview quando quiser validar o resultado
6. Exporte em HTML standalone quando o documento estiver pronto

---

## Estado atual do produto

O projeto ja passou por:

- saneamento dos modelos
- organizacao por nivel de complexidade
- redesign mobile-first
- alinhamento do preview e da exportacao para fundo claro
- rodada de acessibilidade
- rodada de microinteracoes premium
- rodada de UX mobile extrema para telas muito pequenas

---

## Licenca

Defina aqui a licenca do projeto, se aplicavel.
