# HArmonyCa Performance · Design System

Design system do **HArmonyCa Performance** (curso de performance clínica com o injetável híbrido, do ecossistema Facial Academy). Cor predominante **violeta `#7E63C9`**, com azul céu `#3BA7E3` e coral `#D96155` extraídos do gradiente do medidor do logo, mais o navy `#16193C` da tinta do logo; tipografia **Silka** (embutida em woff2, headers em **Medium 500**).

Desenvolvido por **Edegar Junior**.

## Entregas

- **index.html**: design system reutilizável (showcase navegável): paleta (institucional + derivada, com o grupo "Gradiente da marca" e a construção do gradiente do medidor), temas **dark/light**, tipografia (Silka), **gradientes**, **ícones** (Phosphor Thin, copiar SVG), **logos** (copiar/baixar SVG) e sistema de **botões** (variantes/tamanhos/estados; CTA theme-aware via token `--cta`). Click-to-copy em cores, valores e código; download PNG dos gradientes.
  - 🌐 **Online (para compartilhar):** https://eddie-facialacademy.github.io/harmonyca-performance-design-system/ (GitHub Pages, repo público `harmonyca-performance-design-system`).

## Design System portátil (`design-system/`)

Pacote para aplicar a marca em **qualquer projeto/ferramenta** (web, React, Framer, agentes de IA).

- **silka.css**: fonte **Silka** (pesos 300 a 700) embutida em woff2/base64, self-contained; linke antes do CSS principal.
- **harmonyca-performance-design-system.css**: drop-in (tokens dark/light, CTA theme-aware via `--cta` (escuro `#6F56C6`, claro navy `#16193C`) + reset + foco + motion + tipografia + botões + chips/badges/status). Prefixo de classe `hp-`.
- **harmonyca-performance-design-tokens.json**: tokens legíveis por máquina (Style Dictionary, Framer, IA).
- **Button.tsx**: Code Component Framer/React com Property Controls.
- **DESIGN-SYSTEM.md**: spec completa, 3 formas de aplicar e **prompt pronto para IA**.
- **THEME.md**: como o claro/escuro é configurado e ativado pelo tema do sistema do visitante (web + Framer).

## Notas técnicas

- **Cores:** extraídas do **gradiente do medidor do logo** (azul céu `#3BA7E3`, violeta `#7E63C9`, coral `#D96155`) mais o navy `#16193C` (tinta do logo no claro) e o apoio herdado da família (amarelo claro `#FFE4A4`, vermelho claro `#FFB1BD`, amarelado `#FFCA9B`). Derivadas medidas em WCAG AA nos dois temas (varredura com 0 falhas).
- **Logo:** texto nas cores do arquivo (gelo `#F5FAFC` no escuro, navy `#16193C` no claro); o medidor mantém o gradiente oficial e não se recolore.
- **Tipografia:** Silka (institucional), embutida em base64/woff2; Poppins como fallback, depois system-ui. **Headers em Medium (500)**; eyebrow 600; numeral 700; body 300.
- **Ícones:** biblioteca **Phosphor**, peso **Thin** (stroke 1pt na grade 24), `currentColor`.
- **Tema:** dark por padrão; light via `data-theme="light"`; sem atributo segue `prefers-color-scheme`. Toggle persiste em `hp-theme`.
- **Acessibilidade (2 níveis):** (1) texto ≥4.5:1; (2) componente/botão vs fundo ≥3:1 (WCAG 1.4.11). CTA escuro `#6F56C6` (branco 5.5:1, botão vs fundo 3.5:1); CTA claro navy `#16193C`.

## Publicação

Repo público `harmonyca-performance-design-system` (conta `Eddie-FacialAcademy`), branch `main`, `index.html` na raiz, GitHub Pages. `.git` fora do OneDrive (`AppData\Local\gitdirs\`); line-endings LF (`.gitattributes`). Deploy: editar → `git add/commit/push` (credencial no Cofre do Windows, sem token). Ver `HANDOFF.md`.

## CHANGELOG

- **1.0.3** (2026-09-29): CTA escuro `#6F56C6`, dia selecionado do calendário com `--cta-solid`/`--cta-ink`, prévia de tema com o CTA real e seletor de DS com a Facial Premium.
- **1.0.0** (2026-08-28): primeira versão da marca, derivada do molde Facial Academy com paleta do medidor do logo (azul, violeta, coral e navy). Histórico completo em `design-system/CHANGELOG.md`.
