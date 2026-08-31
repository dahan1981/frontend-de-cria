# 01 — Contexto e direção de produto

Use este documento antes de decisões visuais amplas.

## Design começa pela tarefa

Não escolha estética a partir da pergunta “o que está bonito hoje?”. Comece por:

- quem usa;
- em qual ambiente;
- com qual frequência;
- para tomar qual decisão ou executar qual ação;
- qual nível de confiança e precisão é necessário;
- quanto conteúdo precisa caber na tela.

Uma landing page comercial e um sistema fiscal não devem compartilhar a mesma densidade, ritmo ou hierarquia só porque ambos usam React.

## Classifique a superfície

### Operacional

Ex.: ERP, fiscal, financeiro, CRM, painel interno.

Priorize:

- velocidade;
- previsibilidade;
- densidade controlada;
- status claros;
- ações próximas dos objetos;
- tabelas eficientes;
- erros recuperáveis;
- navegação estável.

### Analítica

Priorize:

- comparação;
- contexto temporal;
- filtros visíveis;
- hierarquia de métricas;
- gráficos legíveis;
- explicação de anomalias.

### SaaS de produtividade

Priorize:

- fluxo principal óbvio;
- progressive disclosure;
- empty states que ensinam;
- atalhos para uso recorrente;
- redução de cliques.

### Marketing / conversão

Priorize:

- promessa e prova;
- ritmo editorial;
- direção de arte;
- narrativa;
- CTA inequívoca;
- performance e mobile.

## Contrato de direção

Antes de implementar, defina internamente:

```text
PRODUTO:
USUÁRIO:
TAREFA PRINCIPAL:
EMOÇÃO DESEJADA:
DENSIDADE: baixa | média | alta
DIREÇÃO: ex. editorial sóbria / utilitária premium / técnica precisa
MEMÓRIA VISUAL: o detalhe que diferencia
AÇÃO PRIMÁRIA POR TELA:
```

Não precisa criar um documento extra se isso for pequeno. O objetivo é impedir decisões aleatórias.

## Assumir com responsabilidade

Quando não houver briefing visual:

1. preserve ativos de marca existentes se forem confiáveis;
2. use o domínio do produto para orientar tom e densidade;
3. evite inventar personalidade extravagante para software que exige confiança;
4. registre a hipótese na resposta final se ela afetou decisões relevantes.

## Hierarquia de ação

Uma tela deve responder rapidamente:

- onde estou?
- o que aconteceu?
- o que devo observar?
- o que posso fazer agora?

Evite cinco botões com o mesmo peso visual.

Ação primária deve ser singular ou claramente dominante dentro do contexto da tarefa.

## Menos clique não é sempre melhor

Minimizar interações não significa remover confirmação de ação destrutiva ou esconder opções essenciais. Otimize caminho sem remover segurança.

## Fontes de inspiração

Síntese de princípios de Microsoft Frontend Design Review, exiao Frontend Design/Design Review e OpenAI Frontend App Builder.
