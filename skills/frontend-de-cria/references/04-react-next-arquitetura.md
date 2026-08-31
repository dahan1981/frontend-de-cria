# 04 — React, Next.js e arquitetura de frontend

Aplique apenas quando a stack correspondente existir. Sempre confirme versões no repositório.

## React

### Estado

- não armazene estado que pode ser derivado diretamente de props/estado existente;
- não use `useEffect` para sincronização que pode acontecer durante render ou em event handler;
- mantenha estado o mais próximo possível de quem o usa;
- eleve estado somente quando múltiplos consumidores realmente precisam.

### Componentes

Prefira composição a APIs com dezenas de flags booleanas.

Ruim:

```tsx
<Card compact bordered elevated clickable danger />
```

Melhor: variantes pequenas e composição explícita quando isso melhora clareza.

Não crie componente genérico para uma única ocorrência apenas por estética arquitetural.

### Client boundaries

Em Next.js App Router, não adicione `"use client"` em uma árvore inteira só porque um botão precisa de interação.

Mantenha boundary interativa pequena quando possível.

## Next.js

Confirme a versão real antes de aplicar APIs de caching, routing ou config.

### Server Components

Use Server Components como default quando o projeto já segue App Router e a tela não precisa de interatividade client-side.

### Data fetching

- evite waterfalls independentes;
- faça fetch em paralelo quando as dependências permitem;
- preserve cache/revalidation existentes;
- não mova fetch server-side para `useEffect` apenas para simplificar componente visual.

### Streaming e loading

Use boundaries com intenção. Loading deve manter estrutura e reduzir layout shift, não ser skeleton decorativo infinito.

### Bundle

- evite imports amplos desnecessários;
- use dynamic import para UI pesada quando houver benefício real;
- não adicione bibliotecas grandes para uma microinteração simples.

## Arquitetura por feature

Em apps médios/grandes, módulos de domínio podem agrupar:

```text
features/
  invoices/
    components/
    hooks/
    queries/
    types/
```

Mas respeite a arquitetura existente quando ela já é clara. Não migre o projeto inteiro só para alinhar a uma preferência.

## Contratos

Ao redesenhar, preserve:

- shape de props usados externamente quando possível;
- tipos de API;
- query keys;
- mutation semantics;
- URLs e params;
- server action signatures;
- autorização.

Mudança de interface interna é aceitável quando todos os consumidores são atualizados e comportamento permanece igual.

## Performance e memoização

Não espalhe `useMemo`, `useCallback` e `memo` preventivamente. Otimize onde há custo/re-render relevante ou exigência de identidade estável.

## Fonte de inspiração

Síntese de Vercel Labs React Best Practices/Composition Patterns e PyModel React, Next.js e Feature Architecture.
