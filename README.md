# WimVPN

```
        ░░░░░░░
      ░░░░░░░░░░░
     ░░░░░░░░░░░░░     W I M V P N
    ░░░░░▓▓▓▓░░░░░░    ───────────
   ░░░░░▓▓██▓▓░░░░░░   Quantum-Resistant
   ░░░░▓▓████▓▓░░░░░   AI-Driven VPN
    ░░░▓▓▓▓▓▓▓▓░░░░
     ░░░░░░░░░░░░░      "A whole new world
      ░░░░░▒▒░░░░        of security"
        ░░▒▒▒░░
          ▒▒▒
```

**Next-Generation Post-Quantum VPN Platform**

WimVPN is een VPN-platform volledig gebouwd in Rust met Python AI/ML modellen. Het combineert post-quantum cryptografie, drielaagse symmetrische encryptie, 20 real-time health monitoring algoritmen, een autonome AI Analyst engine en een terminal-stijl Matrix/Aladdin dashboard — in een enkele statisch gelinkte binary.

**Copyright (c) 2026 WimLee115. Alle rechten voorbehouden.**

---

## Overzicht

| Statistiek | Waarde |
|------------|--------|
| Rust codebase | 25.100+ regels |
| Python AI/ML | 2.700+ regels |
| Workspace crates | 14 Rust + 1 Python |
| Tests | 178 (alle groen) |
| Health algoritmen | 20 (4 categorieën) |
| AI correlatie-regels | 8 |
| Threat categorieën | 13 |
| MITRE ATT&CK mappings | 13 |
| Encryptielagen | 3 (ChaCha20 → AES-256 → XChaCha20) |
| Stealth modi | 6 |
| Watermerklagen | 5 |

---

## Post-Quantum Cryptografie

### Hybride Sleuteluitwisseling

Een aanvaller moet **beide** schema's breken:

- **ML-KEM-1024 (Kyber)** — FIPS 203 quantum-safe key encapsulation
- **X25519** — Klassiek ECDH als defense-in-depth
- **HKDF-SHA-512** — Domein-gescheiden sleutelafleiding per encryptielaag

### Hybride Authenticatie

- **ML-DSA-87 (Dilithium5)** — FIPS 204 post-quantum digitale handtekeningen
- **Ed25519** — Klassieke handtekening backup
- **BLAKE3** — Hashing voor fingerprints en integriteit
- **Constant-time vergelijkingen** — `subtle` crate tegen timing side-channels
- **Zeroize** — Automatische geheugenopruiming van geheime sleutels

### Triple-Layer Encryptie

Elk datapakket passeert drie onafhankelijke ciphers in serie:

| Laag | Algoritme | Nonce | Eigenschap |
|------|-----------|-------|------------|
| 1 | ChaCha20-Poly1305 | 12 bytes | Constant-time, software-only |
| 2 | AES-256-GCM | 12 bytes | Hardware-accelerated (AES-NI) |
| 3 | XChaCha20-Poly1305 | 24 bytes | Extended nonce, misuse-resistant |

Overhead per pakket: 96 bytes (48 bytes nonces + 48 bytes authenticatie-tags).

---

## 20 Health Monitoring Algoritmen

Real-time gezondheidsmonitoring over 4 categorieën. Alle algoritmen gebruiken echte runtime metrics (latency, bandwidth, packet loss, CPU, geheugen, key rotations, handshakes).

### Network (6)

| # | Algoritme | Methode |
|---|-----------|---------|
| 1 | Latency Monitor | RTT meting en trendanalyse |
| 2 | Bandwidth Analyzer | Doorvoer tracking en capaciteitsschatting |
| 3 | Packet Loss Detector | Verliesratio monitoring met drempelwaarschuwingen |
| 4 | Jitter Calculator | Inter-packet delay variatie analyse |
| 5 | Stability Index | Samengestelde score: latency + packet loss + key rotations |
| 6 | Congestion Predictor | Latency trend + packet loss + bandwidth variance |

### Security (7)

| # | Algoritme | Methode |
|---|-----------|---------|
| 7 | DNS Leak Detector | Detecteert DNS-queries buiten de tunnel |
| 8 | IP Leak Prevention | IPv4/IPv6-adresblootstelling |
| 9 | WebRTC Leak Guard | STUN/TURN IP-onthulling preventie |
| 10 | Certificate Checker | Certificaatketens en vervaldatum |
| 11 | Protocol Integrity | Pakketstructuur en volgnummer verificatie |
| 12 | Firewall Auditor | Kill-switch firewallregel validatie |
| 13 | Zero-Day Scanner (ML) | Multi-signaal: error spikes + traffic anomalieën + resource abuse + packet ratio |

### Performance (4)

| # | Algoritme | Methode |
|---|-----------|---------|
| 14 | Encryption Perf | Cipher doorvoer en latentie meting |
| 15 | Memory Tracker | RSS- en heap-gebruik monitoring |
| 16 | CPU Balancer | Lastverdeling over encryptiethreads |
| 17 | Route Optimizer (ML) | 4-factor evaluatie: latency + bandwidth + packet loss + key rotation health |

### AI/ML (3)

| # | Algoritme | Methode |
|---|-----------|---------|
| 18 | Traffic Pattern Analyzer (ML) | 3-factor: packet size entropy + inter-arrival variance + bandwidth deviation |
| 19 | Anomaly Detector (ML) | 6-feature: error rate + CPU + memory + packet loss + latency + key rotation |
| 20 | Threat Intel Monitor (ML) | 5-signaal: error rate + amplification + resource pressure + stability + bandwidth |

---

## AI Analyst Engine

Autonome investigatie-engine geïnspireerd op Darktrace:

- **8 correlatie-regels** — DPI Analysis, MITM, Data Exfiltration, Crypto Weakness, DNS Attack, Resource Exhaustion, Bandwidth Throttling, Endpoint Compromise
- **Hypothese-engine** — Template matching, evidence testing, confidence scoring
- **13 threat categorieën** — Elk met MITRE ATT&CK mapping
- **Investigatie lifecycle** — Open → Analyzing → Concluded → Dismissed
- **NLG rapport generator** — Reasoning chains met verdict en tags
- **Alert fatigue reductie** — Max 10/uur, auto-dismiss na herstel

### Python ML Modellen

| Model | Architectuur | Functie |
|-------|-------------|---------|
| EventCorrelationGAT | Graph Attention Network | Event correlatie |
| InvestigationTransformer | Transformer + CLS-token | Threat classificatie |
| HypothesisScorerMLP | 4-laags MLP + BatchNorm | Confidence calibratie |
| AnomalyDetector | Autoencoder | Anomaliedetectie |
| TrafficClassifier | CNN | Verkeersclassificatie |
| ThreatPredictor | LSTM | Dreigingsvoorspelling |
| RouteOptimizerRL | Reinforcement Learning | Route-optimalisatie |
| CongestionPredictor | GRU | Congestievoorspelling |

---

## Traffic Obfuscation

| Feature | Beschrijving |
|---------|-------------|
| HTTPS vermomming | VPN-verkeer verpakt als HTTPS |
| WebSocket vermomming | Verkeer via WebSocket frames |
| DNS-over-HTTPS | Verkeer vermomd als DoH queries |
| Domain fronting | TLS ClientHello SNI-manipulatie via CDN front-domeinen |
| Dekverkeer | Willekeurig dekverkeer maskeert patronen |
| Timing verdediging | Constant-time padding tegen analyse |
| Pakketpadding | Uniforme pakketgrootte |

### Domain Fronting

Echte TLS ClientHello parsing en SNI-vervanging:

- Parseert TLS record header, handshake header, session ID, cipher suites, compression methods, extensions
- Vindt SNI extension (type 0x0000), extraheert hostname
- Vervangt hostname met front domain
- Herstelt alle TLS length-velden (record, handshake, extensions, SNI)

---

## Dashboard

Terminal-stijl Matrix/Aladdin web dashboard op `http://localhost:3000`:

- **Matrix digital rain** — Canvas-gebaseerd met katakana + Arabische karakters
- **CRT/scanline effecten** — Retro terminal-look met glow en flicker
- **ASCII magic lamp logo** — Boot intro met 12 geanimeerde init-regels
- **Real-time health matrix** — 20 algoritmen met kleurgecodeerde scores
- **Bandwidth/latency grafieken** — CSS bar charts (30 datapunten, color-coded)
- **AI Analyst feed** — Live investigations met verdict, tags en confidence
- **SSE streaming** — Real-time updates via Server-Sent Events
- **Token-authenticatie** — Auto-generated token bij opstart

Kleurenschema: matrix green (#00ff41), gold accents (#d4af37), threat red op zwarte achtergrond.

---

## Architectuur

```
                         ┌───────────────┐
                         │  wimvpn-core   │
                         │ (orchestrator) │
                         └───────┬───────┘
                                 │
  ┌──────────┬──────────┬───────┼───────┬──────────┬──────────┐
  │          │          │       │       │          │          │
┌─┴──────┐┌─┴───────┐┌─┴─────┐│┌──────┴─┐┌──────┴─┐┌──────┴──┐
│ crypto ││protocol ││tunnel │││stealth ││ health ││ analyst │
│  (PQ)  ││ (wire)  ││ (TUN) │││(obfsc.)││(20alg.)││  (AI)   │
└────────┘└─────────┘└───────┘│└────────┘└────────┘└─────────┘
                              │
                    ┌─────────┴─────────┐
                    │  wimvpn-dashboard  │
                    │  (Matrix/Aladdin   │
                    │   terminal UI)     │
                    └────────┬──────────┘
                             │
              ┌──────────────┼──────────────┐
              │              │              │
        ┌─────┴────┐  ┌─────┴────┐  ┌──────┴─────┐
        │  client  │  │  server  │  │ watermark  │
        │(CLI+dash)│  │ (multi-  │  │(5-layer PQ)│
        └──────────┘  │ client)  │  └────────────┘
                      └──────────┘
              ┌──────────────┬──────────────┐
              │              │              │
        ┌─────┴────┐  ┌─────┴────┐  ┌──────┴─────┐
        │ adapter  │  │  macros  │  │  wimvpn-ai │
        │(bonding) │  │(proc-mac)│  │  (Python)  │
        └──────────┘  └──────────┘  └────────────┘
```

### 14 Rust Crates

| Crate | Beschrijving |
|-------|-------------|
| `wimvpn-core` | Orchestrator: VPN engine, state machine, kill switch, DNS, split tunneling, metrics collector |
| `wimvpn-crypto` | Post-quantum: ML-KEM-1024 + X25519, ML-DSA-87 + Ed25519, triple-layer encryptie, signed updates |
| `wimvpn-protocol` | Wire protocol: PQ handshake, session management, key rotation, anti-replay |
| `wimvpn-tunnel` | TUN device: async I/O via tokio, gateway management |
| `wimvpn-adapter` | Multi-adapter bonding: failover, round robin, weighted, aggregate |
| `wimvpn-stealth` | Obfuscatie: HTTPS/WebSocket/DoH vermomming, domain fronting met SNI-manipulatie, dekverkeer |
| `wimvpn-health` | 20 health algoritmen in 4 categorieën, ML-gebaseerde heuristics |
| `wimvpn-analyst` | AI Analyst: 8 correlatie-regels, hypothese-engine, 13 threat classes, MITRE ATT&CK |
| `wimvpn-dashboard` | Terminal-stijl Matrix/Aladdin dashboard, SSE streaming, REST API |
| `wimvpn-watermark` | 5-laags watermerk: compile-time BLAKE3, runtime, steganografie, PQ signatures, protocol |
| `wimvpn-macros` | Procedural macro's voor zero-boilerplate configuratie |
| `wimvpn-client` | Client binary: PQ handshake, TUN routing, kill switch, dashboard server |
| `wimvpn-server` | Server binary: multi-client, TUN + NAT, per-client IP allocatie |
| `wimvpn-ai` | Python: 8 ML modellen (GAT, Transformer, MLP, LSTM, GRU, CNN, RL, Autoencoder) |

---

## Quick Start

### Vereisten

- Rust 1.75+ (2021 edition)
- C compiler (voor pqcrypto native libraries)
- Linux (kernel 3.x+ voor TUN ondersteuning)
- Root rechten (sudo) voor TUN device, iptables en route configuratie
- Python 3.10+ met PyTorch (optioneel, voor AI/ML model training)

### Bouwen

```bash
# Bouw alle crates
cargo build --release

# Draai alle tests
cargo test --workspace

# Lint check
cargo clippy -- -D warnings
```

### Server starten

```bash
sudo ./target/release/wimvpn-server \
    --bind 0.0.0.0 \
    --port 51820 \
    --verbose
```

### Client starten

```bash
sudo ./target/release/wimvpn-client \
    --server 127.0.0.1 \
    --port 51820 \
    --stealth-mode https \
    --dashboard-port 3000 \
    --verbose
```

### Dashboard

```
http://localhost:3000
```

Token wordt getoond bij opstart of staat in `/tmp/wimvpn-dashboard-token`.

---

## Feature Scripts

```bash
./20 [token]                    # Health matrix — 20 algoritmen met kleurcoded bars
./On-Device [train|export|all]  # ML pipeline — training, ONNX export, evaluatie
./Triple-Layer [info|verify]    # Cipher stack info en encryptie verificatie
./Traffic [status|test-fronting] # Traffic obfuscation tests
./Web [start|status|test]       # Dashboard management
```

---

## Kill Switch

Fail-closed firewall via dedicated `WIMVPN_KILLSWITCH` iptables chain:

- Blokkeert al het verkeer buiten de VPN tunnel
- DNS leak preventie via `WIMVPN_DNS` chain
- Automatische opruiming bij afsluiting (ook via `Drop` trait)
- Retry logica: 3 pogingen + emergency flush

---

## Dashboard API

| Method | Path | Beschrijving |
|--------|------|-------------|
| GET | `/` | Dashboard SPA |
| GET | `/api/status` | Verbindingsstatus, versie, uptime, cipher suite |
| GET | `/api/metrics` | Live verkeers- en prestatiemetrics |
| GET | `/api/health` | 20 health algoritme rapporten |
| GET | `/api/config` | VPN configuratie |
| POST | `/api/connect` | Verbinding starten |
| POST | `/api/disconnect` | Verbinding verbreken |
| GET | `/api/alerts` | Actieve health alerts |
| GET | `/api/events` | SSE stream real-time updates |
| GET | `/api/analyst/summary` | AI Analyst statistieken |
| GET | `/api/analyst/investigations` | Investigations (filter/paginatie) |
| GET | `/api/analyst/active` | Actieve investigations |
| GET | `/api/watermark/verify` | Watermerk integriteitscheck |

---

## Beveiligingsmodel

| Maatregel | Implementatie |
|-----------|--------------|
| Post-quantum hybride | ML-KEM-1024 + X25519, ML-DSA-87 + Ed25519 |
| Triple-layer encryptie | 3 onafhankelijke ciphers, apart afgeleide sleutels |
| Constant-time crypto | `subtle` crate voor alle vergelijkingen |
| Anti-replay | Sliding window bitmap op inkomende packets |
| Bron-adres validatie | Server valideert packets van verwacht IP |
| Kill switch | Dedicated iptables chains, fail-closed |
| Sleutelrotatie | Automatisch elke 60 seconden |
| Zeroization | Alle geheime sleutels via `Zeroize` trait |
| Security headers | CSP, X-Frame-Options, XCTO, Referrer-Policy |
| 5-laags watermerk | Compile-time, runtime, steganografie, signatures, protocol |

---

## Licentie

**Copyright (c) 2026 WimLee115. Alle rechten voorbehouden.**

Gemaakt door [WimLee115](https://github.com/WimLee115)
