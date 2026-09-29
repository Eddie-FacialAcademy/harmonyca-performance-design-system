# Changelog · HArmonyCa Performance Design System

Todas as mudanças relevantes deste design system são registradas aqui.
O formato segue [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/) e o
versionamento segue [SemVer](https://semver.org/lang/pt-BR/):

- **MAJOR**: muda ou remove um token/API público (quebra compatibilidade).
- **MINOR**: adiciona de forma retrocompatível (novo componente/token/variante).
- **PATCH**: correções que não mudam a API (bug, contraste, ajuste fino).

---

## [Não lançado]

_Nada pendente no momento._

## [1.1.0] · 2026-09-29
### Alterado
- **Nomes de cor organizados em duas camadas.** Cores da marca (`--brand-*`) levam o nome real da cor nesta marca; tokens de uso têm nomes neutros e iguais em todos os DS do grupo (`--primary`, `--accent`, `--highlight`, `--support`, `--glow`), para o código continuar portável entre marcas. Valores não mudaram: comparação de cor computada em todos os elementos do showcase, antes e depois, nos dois temas, deu zero diferença.
- Tokens de uso: `--roxo-bright` → `--primary-bright`, `--lilas-soft` → `--accent-soft`, `--gold-deep` → `--highlight-deep`, `--gold-line` → `--highlight-line`, `--rose-line` → `--support-line`, `--coral-ink` → `--tertiary-ink`, `--gold-ink` → `--highlight-ink`, `--rose-ink` → `--support-ink`, `--azul-luz` → `--secondary-bright`, `--roxo2` → `--primary`, `--lilas` → `--accent`, `--peach` → `--glow`, `--coral` → `--tertiary`, `--roxo` → `--primary-deep`, `--gold` → `--highlight`, `--rose` → `--support`, `--azul` → `--secondary`.
- Cores da marca: `--brand-amarelo` → `--brand-dourado`, `--brand-vermelho` → `--brand-rosa`, `--brand-amarelado` → `--brand-pessego`, `--brand-roxo` → `--brand-violeta`, `--brand-lilas` → `--brand-violeta-luz`, `--brand-azul` → `--brand-azul-ceu`, `--brand-branco` → `--brand-gelo`.
- JSON de tokens: chaves renomeadas igual aos tokens (camelCase) e mapa de/para em `$deprecated`.
- Variantes de botão `hp-gold` e `hp-gold-o` viraram `hp-highlight` e `hp-highlight-o`; os nomes antigos continuam valendo no CSS de colar no site.
- Nomes exibidos no showcase ligados à cor real: acentos compartilhados do grupo como **Dourado claro**, **Rosa claro** e **Pêssego** (antes "Amarelo claro", "Vermelho claro" e "Amarelado", com a mesma cor chamada de formas diferentes entre DS); rótulos de gradiente gerados a partir das cores de cada gradiente.
- Documentação técnica: seção 13 virou "Relação com o molde", só com valores deste DS (a tabela anterior repetia valores de outra marca e desatualizava).
### Descontinuado
- Os nomes antigos listados acima continuam funcionando como apelidos no CSS de colar no site e saem na 2.0. Use os nomes novos em código novo.

## [1.0.3] · 2026-09-29
### Corrigido
- CTA do tema escuro: início do degradê e sólido `#6A50C4` → `#6F56C6`; o botão passava 2.9:1 contra o modal e agora fica ≥3:1; texto branco 5.5:1.
- Dia selecionado do calendário usa `--cta-solid` e `--cta-ink`, no mesmo padrão dos outros DS (aqui o roxo base já passava: 3.6:1 contra o calendário).
- Prévia de tema (cartões escuro e claro) mostra o CTA real de cada tema.
- `--brand-azul`, `--brand-coral` e `--brand-navy` presentes também no showcase (antes só no CSS e no JSON).
- Tabela de acessibilidade do showcase com valores medidos nos dois temas (antes repetia números do molde que não eram desta paleta) e linha nova "CTA contra o fundo" (nível 2).
### Alterado
- Seletor de design systems inclui a Facial Premium, na ordem única usada em todos os DS.
- Versão alinhada em todos os arquivos: tokens, CSS, copy-deck e documentação estavam presos em uma versão anterior ao CHANGELOG.
- Documentação sem travessão e sem "&", com valores de cor, contraste e classe conferidos contra o CSS e o JSON; referências a versões e arquivos inexistentes corrigidas.

## [1.0.2] · 2026-08-28
### Corrigido
- Cor de marca branca alinhada ao arquivo do logo: gelo `#F5FAFC` no lugar do
  `#FFFFFF` absoluto; o swatch de preto absoluto saiu (o escuro da marca é o
  navy `#16193C`).

## [1.0.1] · 2026-08-28
### Alterado
- Menu "Design systems" agora inclui Expert em Lábios 2026.
### Corrigido
- Galeria de gradientes retintada por completo na paleta da marca; o espectro
  agora varre do azul céu ao coral, como o medidor do logo.

## [1.0.0] · 2026-08-28

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
