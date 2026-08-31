# Frontend de Cria

> Um sistema de instruções para fazer o Codex transformar frontends funcionais em interfaces profissionais, sem destruir o que já funciona.

O **Frontend de Cria** não é um template visual e não é uma biblioteca de componentes. É um conjunto compacto de **skills, regras e workflows de design engineering** para agentes de código.

A ideia é simples:

1. você constrói o projeto e faz a lógica funcionar;
2. o backend, autenticação, banco, APIs e regras de negócio já estão prontos;
3. o Codex lê o repositório;
4. consulta este sistema;
5. entende a aplicação antes de tocar no visual;
6. define uma direção estética coerente com o produto;
7. implementa o redesign diretamente no código;
8. testa o resultado no navegador;
9. corrige até o frontend ficar consistente, responsivo e profissional.

**Não existe uma segunda IA reinterpretando o design.** O mesmo agente que decide a direção visual é responsável por implementá-la e validá-la.

---

## O que este repositório resolve

É comum um projeto criado rapidamente chegar a um ponto em que:

* o produto funciona, mas parece protótipo;
* cada tela usa espaçamentos diferentes;
* o dashboard parece genérico;
* tudo virou card;
* formulários ficaram longos e confusos;
* responsividade foi tratada como “diminuir tudo”;
* componentes shadcn foram usados sem uma linguagem visual própria;
* uma IA sugere um redesign bonito, mas outra IA implementa algo diferente;
* uma tentativa de “melhorar o frontend” acaba alterando lógica ou quebrando fluxos.

O Frontend de Cria existe para evitar isso.

---

## Princípio central

> **O frontend atual é referência funcional, não necessariamente referência estética.**

O agente deve preservar o comportamento do produto e pode ser agressivo na refatoração visual quando necessário.

Ele pode mudar layout, hierarquia, composição, tipografia, tokens, componentes, navegação, densidade, tabelas, formulários, modais, estados vazios, loading, responsividade e microinterações.

Ele **não pode alterar silenciosamente**:

* regras de negócio;
* contratos de API;
* autenticação e autorização;
* RLS/policies;
* migrations ou schema de banco;
* regras fiscais, financeiras ou operacionais;
* semântica de validações;
* efeitos colaterais de Server Actions/endpoints;
* integrações externas;
* comportamento do produto só para facilitar o redesign.

Quando um arquivo mistura UI e lógica, a alteração deve ser cirúrgica e comportamentalmente neutra.

---

## Estrutura

```text
frontend-de-cria/
├── AGENTS.md
├── README.md
├── FONTES_E_LICENCAS.md
├── skills/
│   └── frontend-de-cria/
│       ├── SKILL.md
│       └── references/
│           ├── 01-contexto-e-direcao.md
│           ├── 02-sistema-visual.md
│           ├── 03-redesign-app-existente.md
│           ├── 04-react-next-arquitetura.md
│           ├── 05-tailwind-shadcn.md
│           ├── 06-formularios-e-dados.md
│           ├── 07-responsividade-e-acessibilidade.md
│           ├── 08-performance.md
│           ├── 09-qa-visual-e-browser.md
│           └── 10-anti-ai-slop.md
├── workflows/
│   ├── redesign-existing-app.md
│   ├── build-from-scratch.md
│   └── frontend-audit.md
├── templates/
│   ├── AGENTS.project.md
│   └── PEDIDO-PARA-CODEX.md
├── docs/
│   └── DECISOES-DE-ARQUITETURA.md
└── evals/
    └── evals.json
```

### Resolução de caminhos

A pasta oficial de referências é:

```text
skills/frontend-de-cria/references/
```

Alguns workflows podem mencionar arquivos de forma abreviada, por exemplo:

```text
references/01-contexto-e-direcao.md
references/02-sistema-visual.md
references/09-qa-visual-e-browser.md
```

Nesses casos, o agente deve interpretar automaticamente como:

```text
skills/frontend-de-cria/references/01-contexto-e-direcao.md
skills/frontend-de-cria/references/02-sistema-visual.md
skills/frontend-de-cria/references/09-qa-visual-e-browser.md
```

Sempre que aparecer `references/<arquivo>`, considere `skills/frontend-de-cria/references/<arquivo>` como o caminho real.

Em caso de dúvida, **a estrutura real do repositório é a fonte de verdade**.

---

## Como usar com o Codex

### Opção recomendada: colocar este sistema dentro do projeto

O modo mais previsível é fazer o repositório do projeto enxergar fisicamente estas instruções.

Exemplo com submodule:

```bash
git submodule add https://github.com/dahan1981/frontend-de-cria .agents/frontend-de-cria
git submodule update --init --recursive
```

Depois copie/adapte `templates/AGENTS.project.md` para a raiz do projeto como `AGENTS.md`.

Assim o Codex não precisa “lembrar” de procurar outro repositório: as instruções fazem parte do workspace.

### Opção simples: conectar os dois repositórios

Se o ambiente do Codex disponibilizar os dois repositórios na mesma execução, mande-o ler primeiro:

```text
frontend-de-cria/AGENTS.md
frontend-de-cria/skills/frontend-de-cria/SKILL.md
```

E depois executar o redesign no repositório do produto.

### Opção manual

Copie a pasta `skills/frontend-de-cria` para `.agents/skills/frontend-de-cria` no projeto e mantenha um `AGENTS.md` na raiz.

---

## Prompt curto para usar

Depois da instalação, você não precisa escrever um briefing gigante.

Exemplo:

```text
Use o Frontend de Cria para redesenhar este projeto.
Leia o AGENTS.md e a skill antes de alterar arquivos.
Preserve integralmente backend, contratos, autenticação e regras de negócio.
Implemente o redesign no código e valide visualmente antes de concluir.
```

Há uma versão mais completa em `templates/PEDIDO-PARA-CODEX.md`.

---

## Como o agente deve trabalhar

### 1. Descobrir

Antes de editar, mapear:

* framework e versões reais;
* rotas e layouts;
* fronteiras client/server;
* autenticação;
* integrações e APIs;
* componentes compartilhados;
* CSS/Tailwind/design tokens;
* bibliotecas de UI;
* páginas críticas;
* fluxos e estados existentes.

### 2. Proteger

Separar mentalmente o projeto em:

* **protegido:** lógica, contratos e infraestrutura;
* **condicional:** arquivos mistos, tipos compartilhados e Server Actions;
* **livre para redesign:** camada de apresentação.

### 3. Projetar

Definir uma direção visual específica para o produto, não “um SaaS bonito” genérico.

O agente deve considerar contexto, usuário, densidade da interface, tarefa principal e identidade existente antes de decidir o estilo.

### 4. Implementar

O próprio agente implementa suas decisões.

Não entregar apenas:

* mockup;
* descrição visual;
* plano;
* checklist;
* prompt para outro agente.

Quando houver acesso ao código, o resultado esperado é o frontend implementado.

### 5. Verificar

Rodar verificações técnicas e abrir o produto no navegador.

Revisar:

* desktop;
* mobile;
* estados;
* interação;
* console;
* coerência visual;
* responsividade;
* acessibilidade básica.

### 6. Refinar

A primeira renderização não é considerada final.

Depois de visualizar o resultado real, o agente deve corrigir inconsistências, problemas de hierarquia, espaçamento, responsividade e acabamento antes de encerrar.

---

## Padrão de qualidade

Uma implementação não está pronta só porque compila.

Ela precisa ser:

* coerente com o contexto do produto;
* visualmente intencional;
* funcional;
* legível;
* responsiva de verdade;
* acessível;
* consistente entre telas;
* segura em relação à lógica existente;
* sem aparência óbvia de “dashboard gerado por IA”;
* verificada no navegador.

Evite automaticamente:

* excesso de cards;
* gradientes sem função;
* glassmorphism genérico;
* pills em toda parte;
* sidebar de template;
* espaçamento exagerado;
* ícones decorativos sem propósito;
* componentes shadcn usados sem personalização;
* transformar tabelas operacionais em cards só para parecer moderno.

O objetivo não é deixar o projeto “bonitinho”.

O objetivo é fazê-lo parecer **um produto profissional pensado especificamente para o contexto em que será usado**.

---

## Referências especializadas

As referências dentro de `skills/frontend-de-cria/references/` complementam a skill principal.

Use conforme a tarefa:

* `01-contexto-e-direcao.md` — contexto, usuário e direção visual;
* `02-sistema-visual.md` — tokens, tipografia, spacing, superfícies e consistência;
* `03-redesign-app-existente.md` — redesign sem quebrar produto funcional;
* `04-react-next-arquitetura.md` — React, Next.js e arquitetura;
* `05-tailwind-shadcn.md` — Tailwind e shadcn;
* `06-formularios-e-dados.md` — forms, tabelas, filtros e estados;
* `07-responsividade-e-acessibilidade.md` — mobile, teclado, semântica e acessibilidade;
* `08-performance.md` — performance e prevenção de regressões;
* `09-qa-visual-e-browser.md` — validação no navegador e refinamento;
* `10-anti-ai-slop.md` — prevenção de interfaces genéricas de IA.

Não é necessário carregar tudo de uma vez. Leia somente o que for relevante para a tarefa atual.

---

## Workflows

Existem três fluxos principais:

### `workflows/redesign-existing-app.md`

Para produtos já funcionais que precisam de redesign ou modernização.

### `workflows/build-from-scratch.md`

Para criação de uma nova interface ou área ainda não consolidada.

### `workflows/frontend-audit.md`

Para revisão e diagnóstico de um frontend existente.

Se o usuário pedir redesign e houver acesso de escrita ao repositório, a auditoria não deve virar o resultado final. Ela é apenas uma etapa antes da implementação.

---

## Fontes

Este repositório foi construído a partir de uma **síntese e adaptação** de materiais sobre frontend, UX, React, Next.js e design engineering de OpenAI, Microsoft, Vercel Labs, PyModel e exiao.

Consulte `FONTES_E_LICENCAS.md` para proveniência e notas de licença.
