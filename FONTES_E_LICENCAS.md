# Fontes, proveniência e licenças

O **Frontend de Cria** foi escrito como uma síntese original e compacta a partir de cinco pacotes enviados para análise. O objetivo não foi republicar os repositórios inteiros, e sim extrair padrões úteis, remover duplicações e adaptar o conhecimento ao workflow específico de **redesign + implementação pelo mesmo agente**.

## 1. OpenAI — Plugins / build-web-apps

Fonte canônica:

- https://github.com/openai/plugins
- `plugins/build-web-apps/skills/frontend-app-builder`
- `plugins/build-web-apps/skills/frontend-testing-debugging`
- `plugins/build-web-apps/skills/react-best-practices`
- `plugins/build-web-apps/skills/shadcn`

Contribuições conceituais utilizadas:

- agente atua como designer e engenheiro;
- fidelidade entre intenção visual e implementação;
- design system antes de repetição;
- browser QA como parte da implementação;
- frontend testing/debugging.

O snapshot recebido não apresentou uma licença raiz única para todo o repositório. Este projeto usa síntese/adaptação, não uma cópia integral dos arquivos do plugin.

## 2. Microsoft — skills

Fonte canônica:

- https://github.com/microsoft/skills
- `.github/skills/frontend-design-review`

Licença observada no pacote recebido: **MIT License — Microsoft Corporation**.

Contribuições conceituais utilizadas:

- design review estruturado;
- frictionless insight-to-action;
- quality craft;
- direção estética consciente;
- acessibilidade e design-system compliance;
- rejeição de UI genérica sem contexto.

## 3. Vercel Labs — agent-skills

Fonte canônica:

- https://github.com/vercel-labs/agent-skills
- `skills/react-best-practices`
- `skills/composition-patterns`
- `skills/web-design-guidelines`

Contribuições conceituais utilizadas:

- React/Next.js performance;
- composição de componentes;
- revisão de interfaces;
- boundaries e rendering.

O snapshot recebido não apresentou um arquivo LICENSE raiz. Consulte o repositório upstream antes de copiar arquivos literalmente.

## 4. PyModel — react-frontend-skills

Fonte canônica:

- https://github.com/PyModel/react-frontend-skills

Licença observada no pacote recebido: **MIT License — Mohamed Elkholy (Pythoughts), 2026**.

Skills analisadas:

- `ui-design`
- `react`
- `nextjs`
- `typescript`
- `tailwind`
- `shadcn`
- `playwright`
- `react-hook-form`
- `zod`
- `feature-arch`
- `vercel-composition-patterns`
- `vercel-react-best-practices`
- `web-design-guidelines`

Contribuições conceituais utilizadas:

- WCAG e responsive;
- arquitetura por feature;
- Next.js moderno;
- Tailwind v4;
- shadcn;
- forms;
- testes E2E.

## 5. exiao — skills

Fonte canônica:

- https://github.com/exiao/skills
- `design/frontend-design`
- `design/design-review`
- `design/impeccable`
- `coding/adversarial-ux-test`
- `coding/dogfood`

A skill `design/frontend-design` enviada declara **Apache License 2.0** e atribuição ao trabalho que lhe deu origem.

Contribuições conceituais utilizadas:

- contexto antes da estética;
- direção visual intencional;
- critique → refine;
- anti “AI slop”;
- Nielsen heuristics;
- empty states, interaction e responsive.

## Duplicações removidas

Os pacotes possuem sobreposição importante. Exemplos:

- React Best Practices da Vercel aparece direta ou indiretamente em mais de um pacote;
- Web Interface Guidelines aparece em Vercel e PyModel;
- princípios de frontend design aparecem em Microsoft e exiao;
- shadcn/Tailwind aparecem em OpenAI e PyModel.

O Frontend de Cria evita carregar versões repetidas da mesma regra. Quando uma referência ficou redundante, ela foi sintetizada em um único documento.

## Atualização futura

Ao atualizar este repo:

1. consulte as fontes canônicas acima;
2. compare versões e breaking changes de React/Next/Tailwind/shadcn;
3. preserve o workflow central deste projeto;
4. não copie grandes arquivos upstream desnecessariamente;
5. se um trecho for copiado literalmente, preserve a licença/atribuição aplicável;
6. rode os cenários em `evals/evals.json` para verificar regressões de comportamento do agente.
