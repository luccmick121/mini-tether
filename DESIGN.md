---
name: Mini Tether (MUSDT)
description: Landing system do Mini Tether — mundo "cédula/cunhagem" em papel e verde Tether
colors:
  tether-green: "#26A17B"
  link-green: "#1B7D61"
  deep-green: "#0E5A43"
  mint: "#CFE9DD"
  mint-hi: "#A9DEC8"
  paper: "#F7FBF9"
  paper-2: "#EFF7F2"
  card: "#FFFFFF"
  ink: "#0C1F17"
  ink-2: "#41564B"
  ink-3: "#566B5F"
  hairline: "#D7E7DE"
  hairline-soft: "#E4F0E9"
typography:
  display:
    fontFamily: "Bricolage Grotesque, Georgia, serif"
    fontWeight: 800
    lineHeight: 1.02
    letterSpacing: "-0.035em"
  headline:
    fontFamily: "Bricolage Grotesque, Georgia, serif"
    fontSize: "clamp(30px, 4vw, 44px)"
    fontWeight: 800
    lineHeight: 1.08
    letterSpacing: "-0.03em"
  title:
    fontFamily: "IBM Plex Sans, system-ui, sans-serif"
    fontSize: "17px"
    fontWeight: 700
  body:
    fontFamily: "IBM Plex Sans, system-ui, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "IBM Plex Mono, ui-monospace, monospace"
    fontSize: "11px"
    fontWeight: 600
    letterSpacing: "0.14em"
rounded:
  pill: "100px"
  lg: "24px"
  md: "18px"
  sm: "16px"
spacing:
  section: "104px 0"
  wrap: "0 28px (max-width 1120px)"
  gap-sm: "14px"
  gap-lg: "64px"
components:
  button-primary:
    backgroundColor: "{colors.deep-green}"
    textColor: "#FFFFFF"
    rounded: "{rounded.pill}"
    padding: "14px 26px"
  button-primary-hover:
    backgroundColor: "#14604A"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "14px 26px"
  nav-cta:
    backgroundColor: "transparent"
    textColor: "{colors.deep-green}"
    rounded: "{rounded.pill}"
    padding: "8px 16px"
  copy-button:
    backgroundColor: "{colors.deep-green}"
    textColor: "#FFFFFF"
    rounded: "{rounded.pill}"
    padding: "10px 18px"
---

# Design System: Mini Tether (MUSDT)

## Overview

**Creative North Star: "The Mint Note"** — a página é uma cédula: papel claro, guilhoché de anéis concêntricos, selos pill, dados gravados em mono e o verde Tether comprometido em campos inteiros (faixa, seção "how", rodapé), nunca espalhado em detalhes.

Sistema de uma página estática (HTML/CSS/JS único, sem build). A identidade nasce dos assets oficiais (moeda MUSDT + badge do mascote) e do verde da marca (#26A17B), que é reservado para a moeda, ícones e acentos grandes; texto pequeno sobre verde usa o verde profundo (#0E5A43), que contrasta 8.2:1 com branco. Toda afirmação da página é verificável no Etherscan — o sistema visual existe para servir essa prova, não hype.

**Key Characteristics:**
- Campos de verde profundo inteiros delimitam ritmo (faixa de fatos → seção → rodapé).
- Guilhoché de anéis SVG concêntricos como textura de fundo (hero e peg), opacidade ≤ .5.
- Dados on-chain sempre em IBM Plex Mono tabular; rótulos mono 11px em caixa alta.
- Raio pleno em pílulas (100px) para ações e selos; cartões grandes em 24px.
- Ícones SVG autorais, stroke 2, sem emoji e sem biblioteca de glifos.

## Colors

Paleta de um acento (verde Tether) sobre papel neutro esverdeado, com verde profundo como "segundo tinta" de impressão.

### Primary
- **Tether Green** (#26A17B): a moeda, ícones stroke, ::selection, anéis guilhoché, borda de selos. Nunca carrega texto pequeno sobre claro (3.25:1) — nesse papel suba para Link Green.
- **Deep Green** (#0E5A43): campos inteiros com texto branco/mint (8.2:1), botão primário, links sobre escuro, endereço do contrato.

### Secondary
- **Link Green** (#1B7D61): links e acentos de texto sobre superfícies claras (5.06:1).

### Tertiary
- **Mint** (#CFE9DD): texto corrente sobre Deep Green (6.38:1).
- **Mint Hi** (#A9DEC8): números e destaques mono sobre Deep Green (5.45:1).

### Neutral
- **Paper** (#F7FBF9): fundo base da página.
- **Paper 2** (#EFF7F2): seções alternadas (peg, FAQ) e o bloco do endereço.
- **Card** (#FFFFFF): cartões e itens de acordeão.
- **Ink** (#0C1F17): texto primário (16.4:1 no papel).
- **Ink 2** (#41564B): texto secundário (7.9:1).
- **Ink 3** (#566B5F): texto terciário e legendas (5.5:1).
- **Hairline** (#D7E7DE) / **Hairline Soft** (#E4F0E9): divisores e bordas de cartão.

### Named Rules
**The Ink-Stamp Rule.** O Tether Green puro nunca imprime texto pequeno sobre claro; quando o texto precisa de verde, usa Link Green ou Deep Green. O verde puro é tinta de carimbo (moeda, ícone, anel, borda), não de leitura.

## Typography

**Display Font:** Bricolage Grotesque (fallback Georgia, serif)
**Body Font:** IBM Plex Sans (fallback system-ui, sans-serif)
**Label/Mono Font:** IBM Plex Mono

**Character:** display grotesca de personalidade (peso 800, tracking apertado) contra um corpo de trabalho Plex — o par evoca documento impresso oficial, combinando com o mono de dados.

### Hierarchy
- **Display** (800, clamp(42px, 5.6vw, 72px), 1.02, -0.035em): apenas o H1 do hero.
- **Headline** (800, clamp(30px, 4vw, 44px), 1.08, -0.03em): H2 de seção.
- **Title** (700, 15–17px): títulos de cartão, itens de feature, perguntas do FAQ.
- **Body** (400, 16px/1.6): parágrafos; lede do hero em clamp(16px, 1.8vw, 18.5px).
- **Label** (600, 11px, 0.14em, uppercase): rótulos de dados (CONTRACT, NAME, SYMBOL).

### Named Rules
**The Engraved-Data Rule.** Todo dado on-chain (endereço, supply, decimais, pílula 1:1) usa IBM Plex Mono com `font-variant-numeric: tabular-nums`; prosa nunca invade o mono.

## Layout

Container único de 1120px com padding lateral 28px. Seções a 104px de respiro vertical (76px abaixo de 640px). Grid de 2 colunas assimétrico no hero (1.05fr/.95fr) e nas seções why/mascot; listas de features em 2 colunas com divisores hairline (não cartões); facts e specs em grades de 3 colunas com filetes. Quebras: 900px (grids colapsam para 1 coluna) e 640px (grades de specs para 1, links do nav somem). Ritmo: mais espaço acima do H2 que abaixo; alternância de campo claro → faixa escura → claro mantém o compasso de cédula.

## Elevation & Depth

Profundidade por sombra verde com offset e blur (nunca halo de offset zero), sempre no tom #0E5A43 translúcido — a "sombra de impressão" da cédula.

### Shadow Vocabulary
- **Coin lift** (`0 28px 60px -18px rgba(14,90,67,.38)`): moeda e disco do mascote.
- **Soft card** (`0 10px 30px -12px rgba(14,90,67,.22)`): cartões (pair, pílula 1:1, chip do mascote).

### Named Rules
**The Print-Shadow Rule.** Sombras são do tom verde da tinta, com offset ≥ 10px e blur ≥ 30px; sombra decorativa de offset zero é proibida.

## Shapes

Linguagem de cédula: pílulas de raio pleno (100px) para toda ação e selo; cartões grandes em 24px; acordeão e passos em 16–18px. Bordas 1px em Hairline; o único ornamento linear é o anel tracejado (1px dashed, opacidade .45) ao redor do disco do mascote, citando a guilhoché. Imagens de moeda são sempre círculos (border-radius 50%), inclusive logotagos quadrados de terceiros (USDT).

## Components

### Buttons
- **Shape:** pílula (100px), padding 14px 26px, fonte 15px/600.
- **Primary:** Deep Green com texto branco; hover #14604A + translateY(-1px).
- **Ghost:** borda 1.5px Hairline, texto Ink; hover borda Tether Green + texto Link Green.
- **Focus:** `:focus-visible` com outline 2px Tether Green, offset 3px.

### Seal Pill (assinatura)
- **Estilo:** borda 1.5px Tether Green, raio pleno, padding 12px 24px, display 700 16.5px, cor Deep Green, inline-block.
- **Uso:** a frase-assinatura da seção do mascote ("Small, fast, and always ready to work."); anotações de diagrama (tag do par MUSDT=USDT).

### Cards / Containers
- **Corner Style:** 24px (cartões grandes), 18px (passos do ciclo), 16px (FAQ).
- **Background:** Card branco sobre Paper/Paper 2; borda 1px Hairline.
- **Shadow Strategy:** Soft card apenas onde o cartão flutua sobre diagrama.
- **Internal Padding:** 24–56px conforme o cartão.

### Navigation
- Sticky com blur (rgba do papel .9 + backdrop-filter 12px), borda inferior hairline-soft.
- Marca com moeda 34px + wordmark display 800; links 14px/600 Ink 2 (hover Link Green).
- CTA à direita: pílula outline Tether Green "Etherscan ↗" (hover inverte para Deep Green sólido).
- Mobile (<640px): links somem, fica marca + CTA.

### FAQ Accordion
- `details/summary` nativo; item branco raio 16px borda Hairline; ícone "+" SVG autoral que rotaciona 45° no estado aberto; borda vira Tether Green.

### Address Block
- Bloco Paper 2 raio 20px: rótulo mono LABEL, endereço mono tabular em Deep Green (word-break), botão copy pílula e link externo. Nunca fundo escuro-quantizado.

## Do's and Don'ts

### Do:
- **Do** reservar #26A17B para moeda, ícones, anéis e bordas de selo (texto pequeno em verde usa #1B7D61/#0E5A43).
- **Do** apresentar o mascote sempre em disco verde com anel branco (tratamento idêntico ao badge da logo) em TODA renderização da moeda MUSDT — nav, hero, cartões e peg, com badge a ~42% do diâmetro da moeda; nunca branco-sobre-branco e nunca só o mini-badge embutido no PNG.
- **Do** usar IBM Plex Mono tabular para qualquer número on-chain e rótulos em caixa alta 11px/0.14em.
- **Do** manter toda afirmação linkada ao Etherscan; a página nunca pede conexão de carteira.

### Don't:
- **Don't** usar emojis ou glifos Unicode como ícones; ícones são SVG autorais stroke 2.
- **Don't** citar Uniswap ou qualquer DEX; o par é "MUSDT ↔ USDT" e a prova é o Etherscan.
- **Don't** usar fundo preto ou quase-preto; o escuro do sistema é Deep Green #0E5A43.
- **Don't** animar marquee/loop infinito decorativo; movimento é o float da moeda, tilt no ponteiro e reveal de entrada — todos respeitando `prefers-reduced-motion`.
- **Don't** rotular seção com kicker/eyebrow; rótulos mono anotam diagramas (tag do par, rótulo de dado), nunca antecedem headings.
