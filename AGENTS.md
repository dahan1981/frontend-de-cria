# AGENTS.md — Frontend de Cria

Este repositório é um sistema de design engineering para agentes de código.

Quando estiver usando este repositório para trabalhar em outro projeto, leia primeiro:

1. `skills/frontend-de-cria/SKILL.md`
2. apenas as referências apontadas pela skill e relevantes para a tarefa
3. o workflow correspondente em `workflows/`

## Objetivo

Transformar uma interface funcional em uma interface profissional sem mudar silenciosamente o comportamento do produto.

## Regra de ouro

**Preserve comportamento; redesenhe apresentação.**

O frontend existente informa o que o produto faz. Ele não precisa determinar como o produto deve parecer.

## Ordem obrigatória de trabalho

1. Inspecione o repositório alvo antes de editar.
2. Identifique stack, versões, rotas, componentes, estilos, design system e fronteiras client/server.
3. Mapeie os fluxos funcionais que não podem regredir.
4. Classifique arquivos/áreas em `PROTEGIDO`, `CONDICIONAL` e `APRESENTAÇÃO`.
5. Defina uma direção visual apropriada ao produto.
6. Implemente essa direção diretamente no código.
7. Preserve contratos, dados, autenticação, autorização e regras de negócio.
8. Rode lint/typecheck/build/testes disponíveis.
9. Abra a interface no navegador quando houver ambiente executável.
10. Verifique desktop, mobile, estados e console.
11. Faça pelo menos uma rodada de refinamento visual depois da primeira renderização.
12. Só então conclua.

## Não faça

- Não entregue apenas um prompt para outro agente implementar.
- Não pare em uma descrição de redesign quando o repositório pode ser editado.
- Não troque stack ou biblioteca central por preferência pessoal.
- Não reescreva backend para facilitar CSS.
- Não altere schema, RLS, autenticação, endpoints ou regras de negócio sem necessidade funcional explícita.
- Não crie botões, filtros ou ações falsas.
- Não introduza dados fake em fluxos reais apenas para o layout “ficar bonito”.
- Não aplique um template genérico de dashboard em todo projeto.
- Não transforme cada informação em card.
- Não considere compilação equivalente a qualidade visual.

## Prioridade de instruções

Quando houver conflito:

1. requisito explícito do projeto/usuário;
2. preservação de comportamento e segurança;
3. `skills/frontend-de-cria/SKILL.md`;
4. referências deste repositório;
5. preferências estéticas genéricas.

## Comunicação final

Ao concluir uma mudança, informe de forma curta:

- o que foi redesenhado;
- decisões visuais principais;
- arquivos/áreas funcionais preservados;
- verificações executadas;
- qualquer limitação real que permaneceu.
