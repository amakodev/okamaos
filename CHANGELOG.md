# OkamaOS Portal Changelog

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
