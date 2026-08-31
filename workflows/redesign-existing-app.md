# Workflow — Redesign de aplicativo existente

Use para sistemas funcionais que precisam de melhoria visual/UX.

## Fase A — Inventário

1. Leia `AGENTS.md` do projeto alvo.
2. Leia package/configs.
3. Mapeie rotas e layouts.
4. Identifique componentes e tokens existentes.
5. Localize fronteiras de negócio e backend.
6. Se houver app rodando, visite as telas críticas.

Saída interna esperada:

```text
STACK
ROTAS PRINCIPAIS
SHELL
PADRÕES DE UI
FLUXOS CRÍTICOS
ARQUIVOS PROTEGIDOS
ARQUIVOS CONDICIONAIS
ÁREAS DE APRESENTAÇÃO
```

## Fase B — Diagnóstico

Liste os 5-10 problemas de maior impacto, não todos os detalhes cosméticos.

Priorize:

1. arquitetura de informação;
2. fluxo e ações;
3. design system;
4. legibilidade/densidade;
5. consistência;
6. responsividade;
7. polish.

## Fase C — Direção

Defina um contrato visual pequeno usando `references/01-contexto-e-direcao.md` e `02-sistema-visual.md`.

## Fase D — Fundação

Implemente primeiro o que evita divergência:

- tokens;
- CSS global;
- typography;
- shell;
- page header;
- primitives recorrentes.

## Fase E — Superfícies críticas

Redesenhe as rotas de maior valor.

Não pare em uma tela se componentes compartilhados deixarem o restante incoerente.

## Fase F — Estados

Cubra loading, empty, error, disabled e feedback de mutação.

## Fase G — Responsivo

Adapte layout; não apenas reduza tamanhos.

## Fase H — QA

Use `references/09-qa-visual-e-browser.md`.

Rode checks, abra navegador, critique e refine.

## Fase I — Handoff

Resumo final curto:

```text
Redesenhado:
Direção visual:
Preservado:
Verificado:
Limitações:
```
