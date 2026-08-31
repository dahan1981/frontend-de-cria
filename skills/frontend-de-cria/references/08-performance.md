# 08 — Performance de frontend

Design bom precisa sobreviver em produção.

## Antes de otimizar

Meça ou identifique impacto real. Não complique código por micro-otimização especulativa.

## React / Next

### Waterfalls

Quando operações são independentes, inicie em paralelo.

### Client JS

Mantenha Client Components apenas onde interação exige. Não empurre uma árvore inteira para o cliente para facilitar styling.

### Imports

Evite importar pacote inteiro quando há entrypoint menor e estável.

### Componentes pesados

Use lazy/dynamic import quando um recurso caro não é necessário no carregamento inicial.

## Renderização

- derive valores durante render quando simples;
- evite effects de sincronização desnecessários;
- não recrie subscriptions/event listeners sem necessidade;
- use memoização com motivo claro.

## Imagens

- dimensões conhecidas reduzem layout shift;
- responsividade de imagem importa;
- lazy load conteúdo fora da viewport;
- não lazy load automaticamente o principal elemento LCP;
- comprima assets sem destruir qualidade perceptiva.

## Fontes

- carregue apenas pesos necessários;
- prefira formatos modernos;
- evite bloquear render por variedade desnecessária;
- considere font fallback e métricas para reduzir shift.

## CSS e animação

Prefira animar `transform` e `opacity`.

Evite sombras/filtros gigantes animados em muitos elementos.

## Core Web Vitals

Considere:

- LCP;
- CLS;
- INP.

Não trate score isolado como objetivo maior que experiência, mas não aceite regressão óbvia causada pelo redesign.

## Fonte de inspiração

Síntese de Vercel Labs React Best Practices e PyModel React/Next.js/UI Design/Tailwind.
