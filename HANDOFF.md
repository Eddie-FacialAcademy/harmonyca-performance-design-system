# Handoff · HArmonyCa Performance Design System (Versão 1.1.0 · estado em 2026-09-29)

Desenvolvido por **Edegar Junior**. Ponto de retomada; atualizar conforme avançar.

## ✅ Concluído

### Design system online (GitHub Pages)
- **URL pública:** https://eddie-facialacademy.github.io/harmonyca-performance-design-system/
- Repo público `harmonyca-performance-design-system` (conta `Eddie-FacialAcademy`), branch `main`, `index.html` na raiz.
- `index.html`: showcase self-contained, dark/light automático + toggle (chave `hp-theme`), click-to-copy, **copiar/baixar SVG** de logos, **download PNG** dos gradientes, menu "Design systems" entre as marcas e favicon do medidor.

### Marca
- Derivada do molde **Facial Academy** (mesma arquitetura, seções e JS).
- Paleta extraída do **gradiente do medidor**: azul céu `#3BA7E3`, violeta `#7E63C9` (predominante), coral `#D96155`, mais o navy `#16193C` (tinta do logo). Derivadas: violeta profundo `#232755`, violeta intenso `#6A50C4`, violeta luz `#A18FE3`, azul médio `#2A76AD`, azul luz `#5FBBF0`, coral luz `#E8837A` e os tons sobre claro `#5B44AD`/`#1F6FA8`/`#B0453A`. Apoio herdado: amarelo `#FFE4A4`, rosa claro `#FFB1BD`, pêssego `#FFCA9B`.
- **Logo:** wordmark "HArmonyCa Performance" com o medidor (arco + pontos) em gradiente fixo azul→violeta→coral. Composições: horizontal, monocromática (currentColor) e ícone. **Não existe versão vertical.** Texto segue o tema por `currentColor` com as cores do arquivo: gelo `#F5FAFC` no escuro, navy `#16193C` no claro. Não recolorir. Fonte dos arquivos: `Design - Eddie/Facial Academy/64 - HArmonyCa Performance/_ID visual/SVG` (somente a ID visual; o restante da pasta é legado e não se usa).
- **Domínio:** curso do injetável híbrido (produto, indicação, plano de aplicação, resultados). Glossário em `design-system/glossario-marca.md`.

### Acessibilidade (medida, não estimada)
- Pares de contraste da paleta medidos antes do build; varredura renderizada com **0 falhas nos dois temas**.
- CTA por tema: escuro `#6F56C6 → #2A76AD` (branco 5.5:1 e 4.9:1; botão vs fundo 3.5:1 e 4.0:1), claro `#16193C → #5B44AD` (branco 17:1 e 7.3:1).
- Anel de foco em 2 camadas: `--focus-ring` escuro `#A18FE3`, claro `#5B44AD`; guard forced-colors com `outline !important`.

### Pacote portátil (`design-system/`)
- `silka.css` · `harmonyca-performance-design-system.css` (prefixo `hp-`) · `harmonyca-performance-design-tokens.json` · `Button.tsx` · `THEME.md` · `DESIGN-SYSTEM.md` · `IMPLEMENTACAO.md` · `CHANGELOG.md` · `CONTRIBUTING.md` · `copy-deck.harmonyca-performance.json` · `glossario-marca.md` · `voz-e-tom.md`.

## 📌 Próximos passos possíveis
- Landing/página da marca no Framer (subir Color Styles e Text Styles a partir dos tokens).
- Opcionais do roadmap (i18n/RTL, imagery, densidade global) sob demanda.

## Como publicar mudanças
Editar → `git add/commit/push` na `main` (credencial no Cofre do Windows; `.git` em `AppData\Local\gitdirs\harmonyca-performance-design-system`; line-endings LF via `.gitattributes`). O GitHub Pages atualiza sozinho em ~1 minuto.
