# 05 — Tailwind e shadcn/ui

## Primeiro: detecte a realidade do projeto

Leia:

- `package.json`;
- `components.json` quando existir;
- CSS global;
- config Tailwind quando existir;
- componentes em `components/ui` ou equivalente.

Não presuma:

- Tailwind v3 vs v4;
- Radix vs Base UI;
- aliases;
- tokens;
- tema;
- API de primitive.

## Tailwind

### Tokens

Evite replicar valores arbitrários dezenas de vezes.

Prefira transformar decisões recorrentes em CSS variables/theme tokens.

### Classes

Utility-first não significa “cada componente tem um parágrafo de classes sem padrão”.

Extraia componentes/variants quando:

- anatomia se repete;
- estados se repetem;
- manutenção fica propensa a divergência.

Não extraia abstração apenas para reduzir caracteres.

### Responsividade

Use breakpoints e container queries de acordo com composição.

Um componente reutilizado em sidebar e main content pode se beneficiar mais de container query do que viewport breakpoint.

## shadcn/ui

shadcn fornece código base, não identidade de produto.

É esperado adaptar:

- radius;
- cores;
- typography;
- spacing;
- variants;
- anatomia de componentes compostos.

Mas preserve:

- semântica;
- teclado;
- focus management;
- ARIA;
- comportamento dos primitives.

## Radix vs Base UI

Inspecione o código instalado. APIs de composição diferem. Não aplique automaticamente `asChild`, `render` ou padrões de uma implementação na outra.

## Forms

Quando React Hook Form/Zod já estiverem presentes, preserve o schema e a semântica de validação durante redesign. Alterar mensagem/posição visual é diferente de alterar regra.

## Data tables

shadcn não obriga uma estética específica. Evite tabela “demo” com spacing e ações genéricas se o domínio exige densidade, status ou controles específicos.

## Dark mode

Não adicione dark mode automaticamente. Se existir, teste ambos. Se não existir, só introduza quando fizer sentido para o produto/pedido.

## Fonte de inspiração

Síntese de OpenAI build-web-apps shadcn, PyModel Tailwind/shadcn e práticas modernas de Tailwind CSS.
