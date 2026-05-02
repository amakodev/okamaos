# OkamaOS Portal Changelog

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
