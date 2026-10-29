# Guia de estilo: ATCV - Taekwondo Costa Verde

Folha de estilos: `css/style.css`.

## 1. Cores

A paleta parte das cores associadas ao taekwondo e ao clube (preto, vermelho e branco), com dois cinzentos de apoio.

| Nome | Código | Onde se usa |
|---|---|---|
| Preto | `#1a1a1a` | Texto principal, fundo do cabeçalho, do rodapé e dos cabeçalhos da tabela |
| Vermelho | `#b71c1c` | Título principal, ligações, botões, linhas de destaque e página atual no menu |
| Branco | `#ffffff` | Fundo da página e texto sobre fundos escuros |
| Cinzento claro | `#f4f4f4` | Fundo dos cartões das notícias |
| Cinzento de borda | `#767676` | Bordas dos campos do formulário e da tabela |

## 2. Tipografia

| Elemento | Tamanho | Notas |
|---|---|---|
| Família de letra | `"Segoe UI", Arial, Helvetica, sans-serif` | Sem serifa e legível para todas as idades. Usa letras do sistema, por isso não é preciso carregar fontes externas |
| Texto corrente | 1rem (16 px) | Altura de linha de 1,6 |
| `h1` | 2rem (32 px) | Vermelho |
| `h2` | 1.5rem (24 px) | Linha vermelha por baixo |
| `h3` | 1.2rem | |

## 3. Contrastes (WCAG 2.2, nível AA)

Mínimos: 4,5:1 para texto normal e 3:1 para texto grande (a partir de 24 px, ou 18,66 px em negrito). Os rácios foram calculados com a fórmula de luminância relativa do WCAG e podem ser confirmados em https://webaim.org/resources/contrastchecker/

| Utilização | Par de cores | Rácio | Texto normal (4,5:1) | Texto grande (3:1) |
|---|---|---|---|---|
| Texto principal sobre o fundo da página | `#1a1a1a` sobre `#ffffff` | 17,40:1 | Sim | Sim |
| Texto principal sobre os cartões das notícias | `#1a1a1a` sobre `#f4f4f4` | 15,82:1 | Sim | Sim |
| Texto do cabeçalho, do rodapé e dos cabeçalhos da tabela | `#ffffff` sobre `#1a1a1a` | 17,40:1 | Sim | Sim |
| Texto dos botões e da página atual no menu | `#ffffff` sobre `#b71c1c` | 6,57:1 | Sim | Sim |
| Título principal (h1) e ligações | `#b71c1c` sobre `#ffffff` | 6,57:1 | Sim | Sim |
| Ligações dentro dos cartões das notícias | `#b71c1c` sobre `#f4f4f4` | 5,97:1 | Sim | Sim |

Componentes de interface: a cor das bordas (`#767676` sobre `#ffffff`) tem 4,54:1, acima dos 3:1 exigidos para campos de formulário.

**Combinação a evitar:** vermelho `#b71c1c` sobre preto `#1a1a1a` tem apenas 2,65:1 e falha. Por isso, no cabeçalho e no rodapé o vermelho só aparece como linha decorativa, nunca como cor de texto.

## 4. Estados de foco

Todas as ligações, botões e campos têm um contorno de 3 px quando recebem foco com o teclado: preto sobre fundos claros e branco no cabeçalho e no rodapé.
