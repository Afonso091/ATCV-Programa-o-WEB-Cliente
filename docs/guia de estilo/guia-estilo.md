# Guia de estilo: ATCV - Taekwondo Costa Verde

Folha de estilos: `css/style.css`. As cores estão definidas como variáveis CSS no início do ficheiro (`:root`).

## 1. Cores

A paleta é inspirada no logótipo do clube: roxos escuros e vivos, branco, e o verde e o vermelho da bandeira de Portugal apenas como pormenor decorativo.

| Nome | Variável | Código | Onde se usa |
|---|---|---|---|
| Noite | `--cor-noite` | `#27014F` | Texto principal, fundo do cabeçalho e do rodapé, contorno de foco |
| Índigo | `--cor-indigo` | `#4C018B` | Títulos `h1` e `h2`, cabeçalhos da tabela, estado do rato por cima (menu e botões) |
| Ação | `--cor-acao` | `#6502AC` | Ligações, botões, títulos `h3`, datas, página atual no menu e opção marcada nos botões de rádio e caixas |
| Energia | `--cor-energia` | `#A51BEC` | Apenas decoração: barra lateral dos `h2` |
| Borda | `--cor-borda` | `#5C265C` | Bordas dos campos do formulário e do `fieldset` |
| Branco | `--cor-branco` | `#ffffff` | Cartões, tabela, campos, `details` e texto sobre fundos escuros |
| Superfície | `--cor-superficie` | `#f5ecfc` | Linhas pares da tabela |
| Página | `--cor-pagina` | `#f6f0fa` | Fundo da página |
| Verde bandeira | `--cor-verde` | `#046A38` | Apenas decoração: faixa por baixo do cabeçalho |
| Vermelho bandeira | `--cor-vermelho` | `#DA291C` | Apenas decoração: faixa por baixo do cabeçalho |

Cores auxiliares, só para detalhes de interface (não transmitem informação):

| Código | Onde se usa |
|---|---|
| `#e8d6f5` | Contorno dos cartões e do `details`, separadores das linhas da tabela |
| `#efe3f8` | Linha da tabela com o rato por cima |
| `#e4c8ff` | Ligações do rodapé com o rato por cima |

A faixa do cabeçalho tem a proporção da bandeira: 40% verde e 60% vermelho.

## 2. Tipografia

| Elemento | Definição | Notas |
|---|---|---|
| Família de letra | `"Segoe UI", Arial, Helvetica, sans-serif` | Sem serifa e legível para todas as idades. Usa letras do sistema, sem fontes externas |
| Texto corrente | 1rem (16 px) | Altura de linha de 1,6 |
| `h1` | 2rem (32 px) no telemóvel e 2,5rem (40 px) a partir de 768 px | Índigo |
| `h2` | 1,5rem (tamanho por defeito do browser) | Índigo, com barra lateral na cor Energia |
| `h3` | 1,17rem (tamanho por defeito do browser) | Cor Ação |
| Nome do clube no cabeçalho | 1,25rem, negrito | |
| Datas e legendas | 0,9rem | As datas em negrito (peso 600) |
| Rótulos, botões e `summary` | peso 600 | Destacam-se do texto corrente |

Os tamanhos de letra ficam em rem, para respeitarem o tamanho de letra escolhido pela pessoa no browser.

## 3. Modelo de caixa e espaçamentos

**Modelo de caixa.** Todos os elementos usam `box-sizing: border-box`, por isso a largura definida inclui o preenchimento e a borda. O conteúdo de cada página está num `main` centrado, com largura máxima de 900 px.

**Margens, bordas e preenchimentos em px.** Escala de espaçamentos: 8 | 16 | 24 | 32 px. Aplicação:

| Elemento | Regra |
|---|---|
| Títulos, parágrafos, listas, tabelas, figuras, `fieldset` e `details` | Margem de 16 px por baixo, igual em todas as páginas |
| `section` | 32 px de distância entre secções |
| `main` | Preenchimento de 32 px por cima e por baixo, 16 px nos lados (24 px a partir de 600 px e 48 px por cima e por baixo a partir de 1024 px) |
| Cartões (`article`) | Preenchimento de 24 px, margem de 24 px por cima e por baixo, borda de 1 px |
| Grelha de cartões | Espaço de 24 px entre cartões |
| Cabeçalho | 24 px por cima e 16 px nos restantes lados, com faixa de 4 px por baixo |
| Rodapé | 32 px por cima e por baixo, 16 px nos lados |
| Células da tabela | 12 px por 8 px no telemóvel e 12 px por 16 px a partir de 600 px |
| Campos do formulário | Preenchimento de 10 px por 12 px, borda de 2 px |

São usados também ajustes mais pequenos (4, 10, 11 e 12 px) no preenchimento de campos, botões, ligações e células, para um aspeto mais equilibrado.

**Cantos arredondados:** 6 px nos campos, 8 px nas imagens, botões, `details` e tabela, 12 px nos cartões e no mapa, 32 px nos itens do menu e 50% no logótipo.

## 4. Design responsivo (mobile-first)

O CSS base é o do telemóvel. As media queries usam `min-width` e acrescentam regras à medida que o ecrã cresce.

| Ponto de rutura | O que muda |
|---|---|
| Base (menos de 600 px) | Uma coluna, cabeçalho centrado, menu em botões que quebram de linha |
| 600 px | Cartões em 2 colunas, mais espaço nos lados do conteúdo, mais espaço nas células da tabela |
| 768 px | Cabeçalho em linha (logótipo à esquerda, menu à direita) e título maior |
| 1024 px | Cartões em 3 colunas e mais espaço por cima e por baixo do conteúdo |

**Flexbox:** na navegação (`nav ul`), com quebra de linha e centragem. **Grid:** na grelha de cartões das notícias e dos serviços (`.grelha`).

**Imagens:** todas têm `max-width: 100%` e `height: auto`, por isso nunca ultrapassam a largura do ecrã. As imagens fora do ecrã inicial usam `loading="lazy"`.

**Sem deslocação horizontal:** o conteúdo foi testado a 320, 360, 414, 600, 768, 1024, 1280 e 1440 px, sem barra de deslocação horizontal em nenhuma página. O texto quebra palavras demasiado longas (`overflow-wrap`).

## 5. Alvos de toque (mínimo 24 x 24 px CSS)

| Elemento | Tamanho |
|---|---|
| Itens do menu | Preenchimento de 8 px por 16 px, com mais de 40 px de altura |
| Botões e botão de destaque | Preenchimento de 10 a 11 px por 20 a 22 px |
| Botões de rádio e caixas de seleção | 24 x 24 px |
| Ligações do rodapé, das listas e "Saltar o mapa" | Preenchimento de 4 px por 8 px, com mais de 24 px de altura |
| Campos e `summary` | Mais de 24 px de altura |

As ligações dentro de frases estão isentas, segundo o critério 2.5.8 do WCAG 2.2.

## 6. Componentes

**Cabeçalho e menu.** Fundo Noite e faixa verde e vermelha por baixo. O logótipo é circular, com um contorno branco de 3 px, e é uma ligação para a página inicial. Os itens do menu são botões arredondados, com o fundo Índigo quando o rato está por cima. A página atual tem fundo Ação e texto em negrito.

**Botões** (`button` e `.botao`). Fundo Ação, texto branco em peso 600, cantos de 8 px. Com o rato por cima, o fundo passa a Índigo.

**Cartões** (notícias e serviços). Fundo branco, preenchimento de 24 px, cantos de 12 px e contorno fino. O título dentro do cartão não leva a barra lateral.

**Tabelas.** Fundo branco, cabeçalho Índigo com texto branco, separadores finos entre linhas, linhas pares na cor Superfície e realce da linha com o rato por cima. O `caption` fica à esquerda, em negrito, e a tabela ocupa a largura toda.

**Formulários.** Rótulo acima de cada campo, em peso 600. Os campos de texto, o `select` e a `textarea` têm fundo branco, borda de 2 px na cor Borda, cantos de 6 px e largura máxima de 450 px. Os grupos de opções ficam num `fieldset` com `legend`.

Os **botões de rádio e as caixas de seleção** não levam o estilo dos campos de texto: mantêm o aspeto nativo do browser (com 24 x 24 px e a cor Ação quando marcados) e o rótulo fica na mesma linha. Isto evita que desapareçam ou não mostrem a opção marcada em browsers como o Safari, no Mac.

**Elementos HTML5.** `figure` e `figcaption` para imagens com legenda, `time` para datas (em cor Ação), `address` sem itálico e em linha, e `details` com `summary` para as perguntas frequentes.

**Rodapé.** Fundo Noite, texto branco centrado e ligações brancas. Com o rato por cima, as ligações ficam num lilás claro.

## 7. Contrastes (WCAG 2.2, nível AA)

Mínimos: 4,5:1 para texto normal e 3:1 para texto grande e para componentes de interface. Os rácios foram calculados com a fórmula de luminância relativa do WCAG e podem ser confirmados em https://webaim.org/resources/contrastchecker/

### Texto

| Utilização | Par de cores | Rácio | Texto normal (4,5:1) |
|---|---|---|---|
| Texto sobre o fundo da página | `#27014F` sobre `#f6f0fa` | 15,59:1 | Sim |
| Texto sobre cartões, tabela e campos | `#27014F` sobre `#ffffff` | 17,45:1 | Sim |
| Texto sobre as linhas pares da tabela | `#27014F` sobre `#f5ecfc` | 15,19:1 | Sim |
| Texto sobre a linha com o rato por cima | `#27014F` sobre `#efe3f8` | 14,14:1 | Sim |
| Texto do cabeçalho e do rodapé | `#ffffff` sobre `#27014F` | 17,45:1 | Sim |
| Cabeçalhos da tabela e menu com o rato | `#ffffff` sobre `#4C018B` | 12,47:1 | Sim |
| Botões e página atual no menu | `#ffffff` sobre `#6502AC` | 9,73:1 | Sim |
| Títulos `h1` e `h2` sobre a página | `#4C018B` sobre `#f6f0fa` | 11,14:1 | Sim |
| Títulos `h2` dentro dos cartões | `#4C018B` sobre `#ffffff` | 12,47:1 | Sim |
| Ligações e `h3` sobre a página | `#6502AC` sobre `#f6f0fa` | 8,70:1 | Sim |
| Ligações e datas sobre branco | `#6502AC` sobre `#ffffff` | 9,73:1 | Sim |
| Ligações do rodapé com o rato por cima | `#e4c8ff` sobre `#27014F` | 11,64:1 | Sim |

### Componentes de interface (mínimo 3:1)

| Utilização | Par de cores | Rácio | Cumpre |
|---|---|---|---|
| Borda dos campos e do `fieldset` | `#5C265C` sobre `#ffffff` | 11,13:1 | Sim |
| Opção marcada nos botões de rádio e caixas | `#6502AC` sobre `#ffffff` | 9,73:1 | Sim |
| Contorno de foco sobre a página | `#27014F` sobre `#f6f0fa` | 15,59:1 | Sim |
| Contorno de foco no cabeçalho e no rodapé | `#ffffff` sobre `#27014F` | 17,45:1 | Sim |
| Barra lateral dos `h2` (decorativa) | `#A51BEC` sobre `#f6f0fa` | 4,73:1 | Sim |

Os contornos finos dos cartões, do `details` e os separadores da tabela são decorativos: não transmitem informação, porque o conteúdo é sempre identificável pelo texto e pela estrutura. A faixa verde e vermelha também é decorativa.

**Combinações a evitar:**

- Cor Ação sobre Noite: 1,79:1. Por isso, no cabeçalho a página atual é assinalada por fundo **e** negrito, nunca só pela cor.
- Cor Energia (`#A51BEC`) como texto pequeno sobre o cabeçalho: 3,30:1, só serve para texto grande ou decoração.

## 8. Estados de foco e de rato por cima

**Foco com o teclado.** Todas as ligações, botões, campos, `summary` e o mapa têm um contorno de 3 px com um espaço de 2 px: Noite sobre fundos claros e branco no cabeçalho e no rodapé. O contorno nunca é removido. Existe ainda a ligação "Saltar para o conteúdo", que aparece quando recebe o foco.

**Rato por cima.** As ligações passam a Índigo, os botões e itens do menu ganham fundo Índigo, as linhas da tabela ficam com um lilás mais escuro e as ligações do rodapé ficam num lilás claro.
