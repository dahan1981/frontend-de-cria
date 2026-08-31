# Workflow — Auditoria de frontend

Use quando a tarefa for revisar antes de editar ou produzir diagnóstico.

## Passos

1. Entenda tarefa e usuário.
2. Visite/execute interface se possível.
3. Revise arquitetura de informação.
4. Revise hierarquia visual.
5. Revise fluxo e affordances.
6. Revise consistência/design system.
7. Revise forms/data states.
8. Revise responsividade.
9. Revise acessibilidade.
10. Revise performance óbvia.
11. Priorize achados por impacto.

## Escala

### P0 — Bloqueante

Quebra tarefa, segurança, acesso, dados ou interação fundamental.

### P1 — Alto

Confusão significativa, fluxo ruim, informação crítica mal apresentada, mobile quebrado.

### P2 — Médio

Inconsistência, hierarchy, state incompleto, polish que afeta uso.

### P3 — Baixo

Detalhes cosméticos sem impacto relevante.

## Saída

Para cada achado:

```text
[P1] Título
Onde:
Problema:
Impacto:
Correção:
```

Se o usuário pediu redesign e há acesso de escrita, auditoria é apenas fase inicial: implemente as correções depois.
