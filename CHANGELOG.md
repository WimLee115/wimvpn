# Changelog

> *"Every battle makes a Saiyan stronger."* — Vegeta

All notable changes to SaiyanShield will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

### Added
- GitHub Pages landing page with DBZ/Vegeta theme
- Release workflow with multi-platform builds (Linux/macOS/Windows) + Docker
- CI improvements: coverage reporting, MSRV checks

### Changed
- CONTRIBUTING.md and SECURITY.md now bilingual (EN/NL)
- CHANGELOG.md updated with complete history

## [1.0.1-alpha] - 2025-02-18

### Added
- Complete rebrand from WimVPN to **SaiyanShield** (Dragon Ball Z / Vegeta theme)
- Bilingual i18n system in dashboard (EN/NL toggle)
- `data-i18n` attribute system with 80+ translation keys
- Language toggle button in dashboard header
- Bilingual README.md (English first, then Dutch)
- GitHub repos renamed: `saiyanshield-dev` (private), `saiyanshield` (public)

### Changed
- All 14 Rust crates renamed: `wimvpn-*` → `saiyanshield-*`
- Python package renamed: `wimvpn-ai` → `saiyanshield-ai`
- 558 references updated across 117 files
- Dashboard UI rewritten with Saiyan blue/gold/orange color palette
- Ki-energy particle background replaces Matrix digital rain
- Boot sequence with Vegeta quotes and power level scanning
- Iptables chains: `WIMVPN_*` → `SAIYANSHIELD_*`
- Filesystem paths: `/etc/wimvpn/` → `/etc/saiyanshield/`
- Environment variables: `WIMVPN_*` → `SAIYANSHIELD_*`

## [1.0.0-alpha] - 2025-02-17

### Added
- ASCII logo and boot intro sequence to dashboard
- Matrix/Aladdin theme, 11 integration tests
- Terminal-style dashboard rewrite (pure HTML/CSS/JS)
- Edition 2024 upgrade with full clippy compliance

### Fixed
- Score overflow bugs in health algorithms
- CI build: resolved all `-D warnings`
- Python AI tests: added onnxscript dependency and fixed BatchNorm single-sample test
- Cargo fmt formatting across entire workspace

## [0.1.0] - 2025-02-16

### Added
- Initial release
- 14 Rust crates: core, crypto, protocol, tunnel, adapter, stealth, health, analyst, dashboard, watermark, macros, client, server
- 1 Python package: AI/ML pipeline with ONNX
- Post-quantum cryptography: ML-KEM-1024 + X25519, ML-DSA-87 + Ed25519
- Triple-layer encryption
- AI Analyst engine for autonomous threat investigation
- 20 health monitoring algorithms across 4 categories
- Terminal-style web dashboard with real-time SSE
- Kill switch and DNS leak protection
- Traffic obfuscation and stealth mode
- Zero-log architecture with warrant canary
- WireGuard compatibility adapter
- Steganographic watermarking
- Docker and docker-compose support
- CI/CD pipeline with build, test, lint, security audit, benchmarks
- 250+ unit tests
