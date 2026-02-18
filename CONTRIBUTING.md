# Contributing to SaiyanShield

> *"Even a low-class warrior can surpass an elite if he trains hard enough."* — Vegeta

Thanks for your interest in contributing to SaiyanShield! Every contribution increases our power level.

## Getting Started

1. Fork the repository
2. Clone your fork: `git clone https://github.com/<you>/saiyanshield.git`
3. Create a branch: `git checkout -b my-feature`
4. Make your changes
5. Run tests: `cargo test --workspace`
6. Run formatter: `cargo fmt --all`
7. Run linter: `cargo clippy --workspace -- -D warnings`
8. Commit and push
9. Open a Pull Request

## Build Requirements

- Rust 1.85+ (stable, edition 2024)
- OpenSSL development headers (`libssl-dev` / `openssl-devel`)
- Python 3.9+ (for `saiyanshield-ai` crate tests)

## Project Structure

```
saiyanshield/
├── saiyanshield-core/       # VPN engine, kill switch, DNS
├── saiyanshield-crypto/     # Post-quantum cryptography (ML-KEM, ML-DSA)
├── saiyanshield-protocol/   # Custom Noise-based protocol
├── saiyanshield-tunnel/     # TUN/TAP interface
├── saiyanshield-stealth/    # Traffic obfuscation & anti-detection
├── saiyanshield-health/     # 20 health monitoring algorithms
├── saiyanshield-analyst/    # AI correlation & investigation engine
├── saiyanshield-dashboard/  # Terminal-style web dashboard
├── saiyanshield-adapter/    # WireGuard compatibility layer
├── saiyanshield-watermark/  # Steganographic watermarking
├── saiyanshield-macros/     # Procedural macros
├── saiyanshield-client/     # CLI client binary
├── saiyanshield-server/     # Server binary
└── saiyanshield-ai/         # Python ML pipeline (ONNX)
```

## Code Style

- Follow `rustfmt` defaults (see `.rustfmt.toml`)
- All public items should have doc comments
- No `clippy` warnings allowed in CI (`-D warnings`)
- Vegeta quotes in module-level doc comments are encouraged

## Testing

Every PR should include tests for new functionality. Run the full suite with:

```bash
cargo test --workspace
```

## Reporting Issues

Open an issue on GitHub with:
- SaiyanShield version (`saiyanshield --version`)
- OS and architecture
- Steps to reproduce
- Expected vs actual behavior

---

# 🇳🇱 Bijdragen aan SaiyanShield

> *"Zelfs een laagklasse krijger kan een elite overtreffen als hij hard genoeg traint."* — Vegeta

Bedankt voor je interesse om bij te dragen aan SaiyanShield! Elke bijdrage verhoogt ons power level.

## Aan de Slag

1. Fork de repository
2. Clone je fork: `git clone https://github.com/<jij>/saiyanshield.git`
3. Maak een branch: `git checkout -b mijn-feature`
4. Maak je wijzigingen
5. Voer tests uit: `cargo test --workspace`
6. Voer formatter uit: `cargo fmt --all`
7. Voer linter uit: `cargo clippy --workspace -- -D warnings`
8. Commit en push
9. Open een Pull Request

## Vereisten voor Bouwen

- Rust 1.85+ (stable, edition 2024)
- OpenSSL development headers (`libssl-dev` / `openssl-devel`)
- Python 3.9+ (voor `saiyanshield-ai` crate tests)

## Codestijl

- Volg `rustfmt` standaarden (zie `.rustfmt.toml`)
- Alle publieke items moeten doc comments hebben
- Geen `clippy` waarschuwingen toegestaan in CI (`-D warnings`)
- Vegeta quotes in module-level doc comments worden aangemoedigd

## Testen

Elke PR moet tests bevatten voor nieuwe functionaliteit:

```bash
cargo test --workspace
```

## Problemen Melden

Open een issue op GitHub met:
- SaiyanShield versie (`saiyanshield --version`)
- OS en architectuur
- Stappen om te reproduceren
- Verwacht vs daadwerkelijk gedrag
