# Decisão da framework

**Framework escolhida: Bootstrap 5.3.8.**

## Contexto
Comparámos Bootstrap, Foundation e W3.CSS a construir o mesmo componente, um card de notícia (`comparacao.html`). Mediram-se o peso do CSS (separador Rede das DevTools), as linhas de código do card (contagem de linhas) e, com uma escala de 1 a 5, a documentação, a personalização e a acessibilidade por defeito.

## Decisão
O site final mantém o **Bootstrap**.

## Porquê
- **Peso:** o CSS do Bootstrap é o maior (≈ 232 KB sem compressão, ≈ 31 KB com gzip), contra ≈ 23 KB (≈ 5 KB com gzip) do W3.CSS. A diferença existe, mas ≈ 31 KB comprimidos é aceitável para um site de um clube, com poucas imagens e sem grande tráfego móvel.
- **Código:** o card tem 19 linhas nas três frameworks, por isso o esforço de escrita não decide.
- **Documentação (5 contra 4 e 3):** é a mais completa, com exemplos para todos os componentes que o site usa (Navbar, Card, Accordion, Table, Form).
- **Personalização (5 contra 4 e 2):** cada componente expõe variáveis CSS (`--bs-*`), e foi assim que mantivemos o design do clube num ficheiro separado, sem alterar a framework. O W3.CSS não tem variáveis e obrigaria a sobrepor regras uma a uma.
- **Acessibilidade (4 contra 4 e 2):** a Navbar e o Accordion trazem `aria-expanded`, `aria-controls` e navegação por teclado sem código nosso. O W3.CSS não traz nada disto e teria de ser escrito à mão.

## Compromissos aceites
O Bootstrap é mais pesado e o seu aspeto por defeito é reconhecível, o que compensamos com o `style.css`. Se o peso se tornar um problema, a alternativa seria reduzir o CSS carregado (Bootstrap por Sass, só com os módulos usados) e não mudar de framework.
