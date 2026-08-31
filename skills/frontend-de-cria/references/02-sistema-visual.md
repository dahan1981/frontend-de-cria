# 02 — Sistema visual

O objetivo é transformar decisões estéticas em regras repetíveis.

## Tokens primeiro, patches depois

Antes de estilizar dezenas de componentes, consolide o que se repete:

- background;
- surface;
- surface-muted;
- border;
- text-primary;
- text-secondary;
- accent;
- success/warning/error/info;
- radius;
- shadow;
- spacing;
- largura de containers;
- escala tipográfica.

Prefira nomes semânticos a nomes cromáticos.

```css
--background
--surface
--surface-subtle
--border
--foreground
--muted-foreground
--primary
--primary-foreground
--danger
```

é melhor que espalhar `--gray-100`, `--blue-600` diretamente pelas decisões de componente.

## Tipografia

Tipografia é hierarquia, não decoração.

Defina pelo menos:

- display/hero quando existir;
- page title;
- section title;
- body;
- label;
- caption/meta;
- tabular/mono quando dados exigirem.

Em software operacional, tipografia extremamente grande reduz eficiência. Em marketing, escala pode ser mais expressiva.

Não use uma fonte “diferentona” apenas para parecer customizado. Priorize legibilidade e adequação.

## Espaçamento

Use um ritmo limitado e consistente. Exemplo de família:

`4, 8, 12, 16, 24, 32, 48, 64`

Não trate isso como lei matemática. Trate como gramática visual.

Agrupe por proximidade:

- elementos da mesma unidade ficam mais próximos;
- grupos diferentes ganham separação maior;
- seção não precisa de borda se o espaço já organiza.

## Radius

Escolha uma família curta.

Não use radius diferente em cada componente e não transforme tudo em cápsula.

Pills são boas para:

- tags;
- status curtos;
- filtros compactos;
- segmented controls quando coerente.

Não são default para toda ação.

## Bordas e sombras

Sombras servem para comunicar elevação ou separação, não para “deixar premium”.

Em dashboards, uma borda discreta costuma funcionar melhor que múltiplas sombras.

Não combine borda pesada + shadow pesada + gradient + glass em toda superfície.

## Cor

Use uma cor dominante e acentos com função clara.

- status não pode depender só de cor;
- danger precisa ser reservado a danger;
- sucesso não deve virar decoração;
- contraste precisa permanecer legível;
- paletas tímidas demais deixam tudo com o mesmo peso.

## Ícones

Use uma família coerente já presente no projeto ou uma biblioteca consolidada.

Evite misturar SVGs com pesos e estilos incompatíveis.

Ícone sem texto precisa de nome acessível.

## Motion

Motion deve explicar mudança de estado.

Prefira:

- opacity;
- transform;
- transições breves;
- entrada/saída coordenada;
- feedback de interação.

Evite:

- animação em toda coisa clicável;
- bounce/elastic como padrão;
- animar layout pesado sem necessidade;
- movimento que atrasa tarefa operacional.

Sempre respeite `prefers-reduced-motion`.

## Consistência não significa monotonia

O sistema deve permitir variação estrutural. Cards, tabelas, sidebars, listas e painéis podem ter anatomias distintas enquanto compartilham tokens.

## Fonte de inspiração

Síntese de OpenAI Frontend App Builder, Microsoft Frontend Design Review, PyModel UI Design e exiao Frontend Design/Impeccable.
