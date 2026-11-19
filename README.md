# ATCV - Taekwondo Costa Verde

## Grupo
- Afonso Costa (a22603734)
- Simão Gomes (a22510476)
  
## Tema
Site Web responsivo e acessível para a ATCV - Taekwondo Costa Verde, clube de taekwondo de Vila Nova de Gaia. O clube comunicava apenas por Facebook e Instagram e não tinha sítio próprio. O site centraliza serviços, horários, notícias e contactos.

## Público-alvo
Pessoas de todas as idades, de crianças a adultos mais velhos, desde iniciantes a praticantes experientes, e os encarregados de educação das crianças, em Vila Nova de Gaia e arredores.

## Unidade curricular
Programação Web - Cliente, ISLA Gaia. Docente: José Augusto de Araújo Monteiro.

## Framework CSS
- **Bootstrap 5.3.8** (CSS e JavaScript `bundle`), carregado por CDN (jsDelivr) com a versão fixada:
  - `https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css`
  - `https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/js/bootstrap.bundle.min.js`
- O código da framework não foi alterado. Todas as personalizações estão em `css/style.css`, carregado depois do Bootstrap.

### Componentes Bootstrap integrados
1. **Navbar** com menu recolhível em ecrãs pequenos (todas as páginas)
2. **Card** (`servicos.html`, `noticias.html`)
3. **Accordion** nas perguntas frequentes (`servicos.html`)
4. **Table** com `table-striped` e `table-responsive` (`inscreve-te.html`)
5. **Form controls** e **Buttons** (`contactos.html`, `inscreve-te.html`, botões em `index.html`)
6. **List group** (`index.html`) e **Ratio** para o mapa (`contactos.html`)

### Personalizações (`css/custom.css`)
1. Paleta ATCV nas variáveis CSS do Bootstrap (cores, fonte, fundo)
2. Navbar com fundo escuro e separador verde/vermelho
3. Estilo do link ativo da navbar
4. Logótipo redondo com borda branca
5. Botão primário com as cores do clube
6. Cards com cantos arredondados e borda lilás
7. Cabeçalho da tabela personalizado
8. Títulos `h1`/`h2` com cor e barra lateral
9. Acordeão e campos de formulário com borda e foco nas cores do clube
10. Rodapé, foco visível e ligação "Saltar para o conteúdo"

### Grelha Bootstrap (`container`, `row`, `col-*`)
- `index.html`: imagem e texto lado a lado (`col-lg-7/5`, `col-md-5/7`)
- `servicos.html`: `row row-cols-1 row-cols-md-2 row-cols-lg-3` com 3 cards
- `noticias.html`: `row row-cols-1 row-cols-md-2 row-cols-lg-3` com 3 notícias
- `contactos.html`: formulário e informações/mapa em `col-lg-6`
- `inscreve-te.html`: tabela e formulário em `col-lg-5` e `col-lg-7`

## Estrutura
```
index.html, servicos.html, noticias.html, contactos.html, inscreve-te.html
css/style.css
assets/   (imagens)
README.md
```
