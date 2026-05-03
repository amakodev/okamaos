# OkamaOS Portal Changelog

## 2026-05-03 - v2.1.2 game-recovery update package

- Published `okamaos-v2.1.2.okupdate` system update bundle (59 KB / 60,858 bytes).
- Adds update apply confirmation and developer-mode selection for detected `.okupdate` bundles.
- Hides Install / Persistence on installed disk systems unless developer mode is enabled.
- Fixes wallet balance parsing for `0x`, empty, and missing RPC quantity values.
- Adds ranked storage diagnostics for games, saves, update downloads, game downloads, cache, logs, wallet, and controller data.
- Stores game package downloads under `/var/okamaos/downloads` while OS updates stay under `/var/okamaos/updates/downloads`.
- Adds crash-safe game launching with startup watchdog, emergency exit, crash logs, `last-game-status.json`, and framebuffer presentation bootstrap.
- Updated `feed.json`: v2.1.2 "game-recovery" is now latest; v2.1.1 moved to previous.
- SHA-256: `9c4baea06af2171b7a090583ce67aa11cc22eee7dcc41377da77f12e72c87371`

## 2026-05-03 - v2.1.1 package-reliability update package

- Published `okamaos-v2.1.1.okupdate` system update bundle (5 KB).
- Fixes ZIP-format `.ok` package install failures ("not a gzip file") when packages are built by Okama Studio.
- `_is_zip()` now detects all ZIP magic signatures and falls back to `zipfile.is_zipfile()` for edge-case archives.
- `download_game()` validates archive magic bytes after download to catch 404 pages served as HTML.
- Updated `feed.json`: v2.1.1 "package-reliability" is now latest; v2.1.0 moved to previous.
- SHA-256: `7b390ded7c8a6602a4b93f0e961f7650aae361dcff37396289228011bfb705e5`

## 2026-05-02 - v2.0.0 + v2.1.0 packages rebuilt with requirements.txt

- Both packages rebuilt to include `requirements.txt` at bundle root.
- `okama-update apply` now runs `pip install -r requirements.txt` during installation.
- `v2.0.0` deps: `eth-account>=0.8.0`, `mnemonic>=0.20`
- `v2.1.0` deps: `eth-account>=0.8.0`, `mnemonic>=0.20`, `argon2-cffi>=21.3.0`
- Updated SHA-256 and sizes in `feed.json` accordingly.

## 2026-05-02 - v2.1.0 relay-controls update package

- Published `okamaos-v2.1.0.okupdate` system update bundle (42 KB).
- Updated `feed.json`: v2.1.0 "relay-controls" is now latest; v2.0.0 moved to previous.
- SHA-256: `8012cffdc38d79c89a8a01b3dcfcb9d3d187b08bb75d7d3cc9eb9c083717ab34`

## 2026-05-02 - v2.0.0 base-chain update package + blockchain pages

- Published `okamaos-v2.0.0.okupdate` system update bundle (46 KB).
- Updated `feed.json`: v2.0.0 "base-chain" is now latest; v1.3.2 moved to previous.
- SHA-256: `c89c265f93d0d9d3463c047ff4d07bca7b5f908871dcc750e22cd12ecba5c538`
- Added `wallet.html` — MetaMask / manual address connect, ETH + OKT balances, NFT asset grid.
- Added `marketplace.html` — OKAssets NFT marketplace (coming-soon state + how-it-works).
- Added `leaderboard.html` — OKToken play-to-earn rankings with filter bar.
- Updated `index.html`: hero version badge → v2.0.0 base-chain; nav links for Marketplace, Wallet, Leaderboard; update card for v2.0.0.

## 2026-05-02 - v1.3.2 ui-stability update package

- Published `okamaos-v1.3.2.okupdate` system update bundle (35 KB).
- Updated `feed.json`: v1.3.2 "ui-stability" is now latest; v1.3.1 moved to previous.
- SHA-256: `2958569ea63b81ad6b84772fd52aba9e3bc77103e6ccc8d1a401d6faa2c7fffd`

## 2026-05-02 - Mobile-first polish (v2.1.0)

- Fixed: Global `h1` font-size was `clamp(3.25rem, 10.4vw, 8.8rem)` causing page titles to overflow inner pages; reduced to `clamp(2.2rem, 5.5vw, 5rem)` and added `!important` override on `.page-hero h1`.
- Fixed: Canvas animation bleeding through transparent page sections — added `background: var(--ink)` to `main`, `.hero`, `.page-hero`, `.docs-wrap`, `.docs-sidebar`.
- Added: Mobile hamburger nav (≤720px) with animated X toggle, full-width dropdown, Escape to close, focus return — wired in all pages via `app.js initMobileNav()`.
- Added: "Get OkamaOS" download section on index.html with three installation paths: Live USB (Balena Etcher), VirtualBox VM, and Build from source — each with numbered step-by-step guides.
- Added: Studio CTA bar on the download section linking to `https://okamaos.zyntrix.solutions`.
- Updated: All "Open Studio" header-action buttons across all pages now link to `https://okamaos.zyntrix.solutions`.
- Updated: Creator section on index.html rewritten to focus on Studio as the game-building entry point.
- Fixed: Docs sidebar breakpoint changed from 860px to 640px so sidebar stays visible on typical desktop/tablet widths.
- Fixed: `overflow-x: hidden` on `body` prevents horizontal scroll on mobile.
- Fixed: `@media (max-width: 520px)` improvements for install cards, eco-grid, studio CTA bar.

## 2026-05-02 - Ecosystem Hub (v2.0.0)

- Full site overhaul: portal is now the source of truth for the entire OkamaOS ecosystem.
- Added `docs.html`: comprehensive OS documentation hub — architecture, boot sequence, package format, build guide, OTA updates, controllers, Bluetooth, and security model. Sticky sidebar with IntersectionObserver active section tracking.
- Added `packages.html`: full command reference for `okama-cli`, `okama-pack`, `okama-update`, `okama-install`, `okama-run`, `okama-shell`, `okama-inputd`, `okama-agent`, and the developer console.
- Added `changelog.html`: full release history for OS, Studio, and the portal with component filter buttons (OS / Studio / Portal).
- Added `studio.html`: Okama Studio landing page with feature overview, getting started guide, API key setup, AI agent tool reference, dev server deployment guide, and Learn Hub summary.
- Updated `index.html`: new nav (Docs, Packages, Studio, Games, Updates, Changelog), ecosystem overview cards section, v1.3.0 hero with Studio v0.3.0 status panel, improved creator section, expanded footer.
- Updated `styles.css`: new component styles for eco-grid, docs-wrap, pkg-section, cl-entry, filter buttons, feature cards, step-grid, tool-grid, and inner page hero.
- Updated `app.js`: fallback data updated to v1.3.0; canvas animation and catalog/update loading made conditional by element presence — shared cleanly across all pages.

## 2026-05-02 - devlink (v1.3.0)

- Published `okamaos-v1.3.0.okupdate` system update bundle.
- Updated `feed.json` to point at v1.3.0 with SHA-256 and size metadata.
- Fixes: ZIP `.ok` package install (Okama Studio builds), key-hold navigation repeat, dev console ANSI escape codes, dev console command tail-scroll.
- Feature: Game Store custom server URL entry (X button) for dev-server wireless game hosting.
- Previous v1.0.2 archived in `previous` array in feed.json.

## 2026-04-29 - Safe System Update

- Published a real `okamaos-v1.0.2.okupdate` system update bundle.
- Updated the feed to point at an installable runtime update artifact.
- Added safe-upgrade notes for preserving games, saves, settings, and update history.

## 2026-04-29 - First Wave Notify

- Added a downloadable `okamaos-v1.0.1.okupdate` manifest to the public update channel.
- Updated the feed with OS and game update notification release notes.
- Updated the demo game catalog entry to `0.1.1` so installed `0.1.0` demo games can receive update notices.

## 2026-04-29 - First Wave v1

- Added a downloadable `okamaos-v1.0.0.okupdate` manifest to the public update channel.
- Updated the portal update feed to point current users at the v1 download.
- Replaced homepage text branding with the OkamaOS logo asset.
- Added boot-screen and runtime-logo notes for the v1 release.

## 2026-04-29 - Launch Hub

- Published the first OkamaOS public portal design.
- Added the app catalog section with a real demo `.ok` download.
- Added the public update feed section for OS release metadata.
- Added creator-facing copy for early game drops.
- Added static JSON feeds for catalog and update clients.
