# 06 — Formulários e interfaces de dados

## Formulários

Formulário profissional não é uma pilha de inputs.

### Estrutura

- agrupe campos por intenção;
- use labels persistentes;
- coloque ajuda perto do campo quando necessária;
- diferencie obrigatório/opcional sem ruído;
- mantenha ordem de teclado lógica;
- use tipos/autocomplete corretos.

### Validação

- erro deve dizer o que aconteceu e como corrigir;
- não apague valor digitado após falha;
- associe mensagem ao campo;
- validation timing deve evitar agressividade enquanto usuário ainda digita;
- erro de servidor precisa ser distinguível de erro de campo.

### Ações

- botão principal precisa refletir a ação real: `Salvar empresa`, `Emitir nota`, etc.;
- loading deve impedir dupla submissão quando necessário;
- ação destrutiva deve ter peso e confirmação adequados ao risco;
- cancel/back deve ser previsível.

### Formulários longos

Considere:

- seções;
- steps apenas quando melhoram compreensão;
- sticky action footer em desktop para tarefas extensas;
- resumo de erro;
- autosave somente se tecnicamente seguro e transparente.

Não crie wizard para qualquer formulário com 8 campos.

## Dados

### Status

Status precisa combinar:

- texto;
- cor;
- eventualmente ícone;
- tooltip quando o significado não for óbvio.

Nunca use cor como único sinal.

### Valores numéricos

- alinhe comparáveis;
- use locale do produto;
- considere tabular numerals;
- mantenha unidade e moeda inequívocas.

### Filtros

Filtros frequentes devem permanecer acessíveis.

Use:

- busca para texto amplo;
- select/combobox para taxonomias;
- date range para períodos;
- chips apenas quando ajudam a visualizar filtros ativos.

Forneça forma clara de limpar filtros.

### Ações de linha

Ação mais frequente pode ficar visível. Ações raras podem ir para menu contextual.

Não coloque tudo em três pontos se o usuário executa aquela ação o dia inteiro.

### Empty state

Um bom empty state responde:

- por que não há dados?
- isso é normal?
- qual próximo passo existe?

Diferencie “nenhum registro cadastrado” de “nenhum resultado para os filtros”.

### Loading

Skeleton deve aproximar a estrutura final para evitar salto. Em ações locais, spinner/estado no controle pode ser melhor que bloquear tela inteira.

### Error state

Erro deve preservar contexto e oferecer recuperação quando possível.

## Fonte de inspiração

Síntese de PyModel UI Design/shadcn/react-hook-form e princípios de Microsoft/exiao sobre frictionless UX.
