# Changelog — HArmonyCa Performance Design System

Todas as mudanças relevantes deste design system são registradas aqui.
O formato segue [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/) e o
versionamento segue [SemVer](https://semver.org/lang/pt-BR/):

- **MAJOR** — muda ou remove um token/API público (quebra compatibilidade).
- **MINOR** — adiciona de forma retrocompatível (novo componente/token/variante).
- **PATCH** — correções que não mudam a API (bug, contraste, ajuste fino).

---

## [Não lançado]

_Nada pendente no momento._

## [1.0.0] — 2026-08-28

Primeira versão do HArmonyCa Performance, derivada do molde Facial Academy.
Paleta extraída do gradiente do medidor do logo (azul céu `#3BA7E3`, violeta
`#7E63C9`, coral `#D96155`) mais o navy `#16193C` da tinta do logo, com
derivadas medidas em WCAG AA nos dois temas.

### Marca
- Logo horizontal, versão monocromática e ícone (medidor) embutidos como
  `symbol` SVG; texto segue o tema por `currentColor` com as cores do arquivo
  (gelo `#F5FAFC` no escuro, navy `#16193C` no claro), medidor mantém o
  gradiente oficial.
- Favicon com o medidor em badge navy `#16193C`, SVG data-URI no `head`.

### Fundações
- Tema escuro com fundos navy (`#0A0C1B` a `#1E2246`) e tema claro off-white;
  paridade total e contraste **WCAG AA** medido (varredura 0 falhas nos dois
  temas).
- CTA por tema: escuro `#6A50C4 → #2A76AD` (violeta intenso para azul médio),
  claro `#16193C → #5B44AD` (navy para violeta); acessibilidade em 2 níveis.
- Anel de foco em duas camadas (`--focus-ring` escuro `#A18FE3`, claro
  `#5B44AD`) e guard de alto contraste com `outline` `!important`.
- Tokens `--azul`, `--azul-luz`, `--coral` e `--coral-ink` para as cores do
  medidor; prefixo de classe `hp-`; tema em `localStorage` na chave `hp-theme`.
- Seção Cores com o grupo "Gradiente da marca": construção do gradiente do
  medidor (80°, três paradas) e dos derivados de CTA, com receita CSS.

### Produto
- Copy de demonstração no domínio do curso: produto híbrido, indicação, plano
  de aplicação, casos e resultados (ver `glossario-marca.md`).
- Forms, feedback, overlays, estrutura e componentes avançados herdados do
  molde, com matriz de estados e a11y de teclado.

### Navegação do showcase
- Menu "Design systems" com as marcas do ecossistema e scrollspy por
  categorias, herdados do molde.
