# Decisões de arquitetura do Frontend de Cria

## Por que não juntar todos os `.md` dos 5 ZIPs?

Porque volume não equivale a contexto útil.

Os pacotes recebidos possuem milhares de arquivos fora do escopo (Azure, App Store, vídeo, analytics, etc.) e diversas duplicações de React, web guidelines e design.

Carregar tudo faria o agente:

- gastar contexto;
- receber regras repetidas;
- encontrar orientações conflitantes;
- ter mais dificuldade para saber qual regra domina;
- potencialmente aplicar workflow de uma ferramenta ausente.

## Por que uma skill central + referências?

É o modelo de progressive disclosure:

- `SKILL.md` contém workflow e decisões de roteamento;
- references são lidas apenas quando necessárias;
- workflows dão sequências específicas;
- `AGENTS.md` garante comportamento persistente no repo.

## Por que o redesign e a implementação ficam no mesmo agente?

Para evitar perda de intenção entre uma IA que “desenha” e outra que interpreta um prompt e implementa.

Neste sistema, o spec é transformado imediatamente em código pelo mesmo agente e verificado pelo render real.

## Por que preservar backend explicitamente?

O uso principal esperado é pós-backend: produto funcional que precisa de acabamento visual.

Sem uma boundary clara, agentes podem alterar data fetching, schemas, auth ou contracts para facilitar uma refatoração de UI. Isso aumenta risco e torna o redesign difícil de auditar.

## Por que não forçar ImageGen?

Um conceito visual pode ser útil, mas não é dependência universal e pode criar mais um artefato a ser reinterpretado.

Para este workflow, a fonte de verdade é:

- contexto do produto;
- design contract;
- código;
- browser render;
- rodada de refinamento.

Se o ambiente tiver geração de conceito visual e ela ajudar, pode ser usada, mas não bloqueia o trabalho.
