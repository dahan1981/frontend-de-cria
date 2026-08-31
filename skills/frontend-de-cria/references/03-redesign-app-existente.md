# 03 — Redesign de aplicativo existente

Este é o cenário principal do Frontend de Cria.

## O código atual tem dois valores diferentes

### Valor funcional

Ele revela:

- fluxos;
- dados;
- ações;
- permissões;
- estados;
- integrações;
- contratos.

Preserve isso.

### Valor estético

Pode ser baixo, inconsistente ou temporário.

Não preserve automaticamente:

- spacing ruim;
- hierarquia confusa;
- componentes duplicados;
- uso excessivo de cards;
- paleta arbitrária;
- layout herdado de boilerplate;
- estética default de shadcn.

## Faça inventário antes de refatorar

Mapeie:

- shell global;
- sidebar/nav/header;
- layouts de página;
- padrões de título e ações;
- tables/lists;
- forms;
- filters/search;
- dialogs/drawers;
- feedback/status;
- empty/loading/error;
- telas críticas.

Depois encontre as inconsistências que se repetem. Corrigir uma regra-base vale mais que remendar 20 páginas.

## Ordem de redesign recomendada

1. tokens e typography;
2. app shell;
3. page header e containers;
4. primitives reutilizados;
5. padrões de dados/forms;
6. telas principais;
7. estados e detalhes;
8. mobile;
9. QA visual.

## Não faça “big bang” sem necessidade

Se o app é grande, trabalhe por sistemas e superfícies. Uma refatoração visual coerente pode acontecer em etapas sem reescrever todo o projeto.

## Preserve affordance

Ao deixar uma tela “clean”, não esconda:

- filtros frequentes;
- status operacionais;
- ações de linha importantes;
- contexto de erro;
- campos necessários;
- histórico útil.

Minimalismo não é remover informação. É organizar o que merece atenção.

## Software data-heavy

### Tabelas

Use tabela quando o trabalho envolve comparação entre linhas/colunas.

Não converta tabela automaticamente em cards.

Boas decisões podem incluir:

- header sticky;
- coluna de ação consistente;
- alinhamento numérico à direita;
- tabular numerals;
- filtros acima da tabela;
- density confortável;
- seleção explícita;
- paginação ou virtualização quando necessário;
- truncation com acesso ao valor completo.

### Dashboard

Não comece pela fórmula “4 KPI cards + gráfico + atividade recente”.

Pergunte qual decisão o dashboard suporta.

Algumas métricas merecem card. Outras funcionam melhor como resumo inline, lista de pendências, status operacional ou tabela.

### Sidebars

Sidebar deve refletir arquitetura do produto, não quantidade de rotas.

Agrupe por tarefa e domínio. Evite separadores e labels em excesso.

## Estados

Todo fluxo real precisa considerar:

- zero data;
- loading;
- erro de carregamento;
- erro de mutação;
- sucesso;
- disabled;
- permission denied;
- item inexistente quando aplicável.

## Alterações estruturais permitidas

É aceitável:

- extrair componentes;
- reorganizar JSX;
- separar layout visual;
- criar tokens;
- unificar primitives;
- mover estilos;
- simplificar props visuais.

Não é aceitável usar “refatoração visual” como justificativa para mudar comportamento de negócio sem pedido.

## Fonte de inspiração

Síntese de OpenAI Frontend App Builder/Testing, Microsoft Frontend Design Review e exiao Design Review/Polish.
