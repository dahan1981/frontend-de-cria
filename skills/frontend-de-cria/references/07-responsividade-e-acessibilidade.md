# 07 — Responsividade e acessibilidade

## Responsividade é adaptação

Não reduza simplesmente o desktop.

Pergunte em cada breakpoint:

- qual informação continua crítica?
- qual ação continua frequente?
- o que pode mudar de posição?
- o que pode colapsar sem desaparecer?
- a navegação precisa mudar de formato?

## Mobile

### Não ampute funcionalidade

Evite esconder função crítica em mobile só porque não cabe.

Alternativas:

- drawer;
- sheet;
- disclosure;
- resumo + detalhe;
- scroll horizontal consciente para tabelas;
- ações sticky;
- cards apenas quando a leitura linha-a-linha for mais importante que comparação tabular.

## Touch

Alvos interativos devem ser confortáveis. Use aproximadamente 44x44 CSS px quando aplicável para controles touch importantes.

## HTML semântico

Prefira elementos nativos:

- `button` para ações;
- `a` para navegação;
- `label` associado a input;
- headings em ordem lógica;
- landmarks (`main`, `nav`, `aside`, etc.).

Não recrie button acessível com `div` clicável.

## Teclado

Fluxos essenciais precisam funcionar sem mouse.

Verifique:

- ordem de tab;
- foco visível;
- dialogs/drawers;
- menus;
- comboboxes;
- tabelas interativas;
- escape/cancel quando esperado.

## ARIA

ARIA complementa HTML nativo; não substitui semântica.

Controles icon-only precisam de nome acessível.

## Contraste

Mantenha contraste suficiente para texto e controles. Não use cinza claro demais apenas para atingir estética “clean”.

## Cor

Não comunique erro, sucesso ou status somente por cor.

## Motion

Respeite `prefers-reduced-motion` e evite motion necessário para entender conteúdo.

## Fontes e legibilidade

- body deve permanecer confortável em mobile;
- line-height suficiente;
- não force blocos de texto largos demais;
- textos críticos não devem depender de hover.

## Fonte de inspiração

Síntese de PyModel UI Design, Microsoft Frontend Design Review, Vercel Web Interface Guidelines e exiao responsive/interaction guidance.
