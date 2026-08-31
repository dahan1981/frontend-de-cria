# 09 — QA visual e navegador

Compilar é necessário; não é suficiente.

## Loop obrigatório quando há app executável

1. descubra script correto;
2. rode lint/typecheck/build/testes relevantes;
3. inicie app;
4. abra a rota principal;
5. verifique console;
6. percorra fluxos críticos;
7. capture/observe desktop;
8. capture/observe mobile;
9. critique visualmente;
10. corrija;
11. repita.

## Checks visuais

### Hierarquia

- título e ação principal são óbvios?
- informação secundária está realmente secundária?
- existem elementos competindo sem necessidade?

### Spacing

- gutters são consistentes?
- cards/sections têm padding coerente?
- grupos relacionados parecem grupos?
- existe espaço excessivo desperdiçado em software operacional?

### Typography

- tamanho/peso segue escala?
- labels/metas são legíveis?
- números e tabelas mantêm alinhamento?

### Componentes

- buttons têm estados hover/focus/disabled/loading?
- inputs têm focus/error?
- menus e modais funcionam?
- ícones estão alinhados e coerentes?

### Estados

Teste quando possível:

- empty;
- loading;
- error;
- sucesso;
- dado longo;
- lista grande;
- permissão limitada.

## Viewports mínimos sugeridos

Quando não houver matriz do projeto:

- desktop amplo: ~1440 px;
- notebook: ~1280 px;
- mobile: ~390 px.

Adicione tablet se a composição mudar significativamente.

## Console

Não ignore:

- hydration warnings;
- React key warnings;
- network errors introduzidos;
- exceções em interação;
- accessibility warnings úteis.

## Testes E2E

Se Playwright já existir, reutilize padrões do projeto. Não reescreva suíte só por redesign.

Seletores devem preferir roles/names/test IDs estáveis conforme estratégia existente.

## Antes/depois

Em redesign grande, compare mentalmente ou por screenshot:

- tarefa ficou mais clara?
- densidade ficou adequada?
- ações ficaram previsíveis?
- algum dado sumiu?
- algum fluxo ficou mais longo?
- a nova tela parece parte do mesmo produto?

## Critério de parada

Não pare no primeiro render aceitável. Pare quando não houver problemas visuais óbvios, regressões funcionais conhecidas ou inconsistências que o próprio agente percebeu.

## Fonte de inspiração

Síntese de OpenAI Frontend Testing Debugging/App Builder, PyModel Playwright e exiao Design Review.
