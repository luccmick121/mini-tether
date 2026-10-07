# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Static single-file HTML/CSS/JS (no build), served by GitHub Pages from this repo
(CNAME minitether.duckdns.org). Fonts via Google Fonts CDN.

## Users

- Crypto-curious visitors who see the MUSDT token referenced somewhere (Etherscan,
  a wallet, social) and land here asking: what is this coin, why does it exist,
  and is it legitimate.
- Operators of the house (the project treasury) who point people to one canonical
  URL with the verified contract address.

## Product Purpose

Mini Tether (MUSDT) is an ERC-20 on Ethereum mainnet that tracks USDT 1:1 through
on-chain liquidity and is branded for micro-transactions (tipping, fractions of a
cent, pay-per-use). The site's single job: present the coin's identity (logo,
mascot badge), explain WHY it exists, and route the visitor to independent
verification on Etherscan. Success = visitor understands the coin and clicks
through to the verified contract.

## Positioning

A mirror-clean TetherToken: verified source, ERC-20 surface only — no mint, no
pause, no blacklist, no proxy — with a vanity address (dac1…1ec7) adjacent to real
USDT. The only owner functions are cosmetic (setName/setSymbol/transferOwnership).

## Operating Context

- Contract (source of truth, from addresses.ethereum.json):
  `0xdAC15c8B27CC1D0AEC5c28F568D7664da0401ec7` — verified on Etherscan.
- Supply 100,000,000,000 fixed at deploy; decimals 6 (same as USDT).
- Pool live at price 1.000000 (15∥15) — per docs/HANDOFF-LAYA-2026-10-07.md.
- Site repo: github.com/luccmick121/mini-tether (GitHub Pages, CNAME).

## Capabilities and Constraints

Content rules fixed by the operator (2026-10-07 brief):
- NO mention of Uniswap (or any DEX) anywhere on the page.
- NO wallet-connect feature of any kind.
- NO emojis; icons must be proportional SVG.
- Light theme: greens, NO black backgrounds.
- Etherscan links are the external proof surface.
- Every on-chain claim must be true against contracts/TetherTokenV3.sol
  (functions: ERC-20 + setName/setSymbol/transferOwnership ONLY).
Undecided: language stays English (incumbent choice; operator speaks PT-BR).

## Brand Commitments

- Official logo: assets/mini-tether/formatos/logo-*.png (T-monet + mascot badge,
  transparent bg) — FINAL version, already in this repo as logo-*.png.
- Mascot badge: badge-mascote.png ("The Mini Dollar") must be presented visibly
  (the incumbent site renders it nearly invisible).
- Tether green #26A17B is the anchor color; paper-white surfaces.

## Evidence on Hand

- Verified contract + address (addresses.ethereum.json, HANDOFF doc).
- Real pool state (price 1.000000, reserves 15∥15) as of 2026-10-07.
- Logo pack (16→1024px), favicon, master SVG, USDT logo (self-hosted usdt.png).
- No testimonials, no socials, no team page — do not fabricate any.

## Product Principles

1. Truth over hype: every claim checkable against the verified source in one click.
2. The coin is the hero: identity (logo + badge) leads, text explains why.
3. Verification is the CTA: Etherscan is the destination, not a wallet.
4. Micro is the story: precision of 6 decimals, small payments, the mascot's world.

## Accessibility & Inclusion

Standard web a11y: contrast ≥4.5:1 body text, keyboard-focusable controls,
reduced-motion respected. No product-specific requirement established.
