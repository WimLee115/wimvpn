# Security Policy

> *"Only a fool trusts his opponent to play fair."* — Vegeta

## Reporting a Vulnerability

If you discover a security vulnerability in SaiyanShield, please report it responsibly.

**Do NOT open a public issue.**

Instead, email: **security@saiyanshield.dev**

You will receive a response within 48 hours. We will work with you to understand the issue and coordinate a fix before any public disclosure.

## Supported Versions

| Version | Supported |
|---------|-----------|
| latest  | Yes       |

## Security Measures

SaiyanShield implements the following security measures:

- **Post-quantum cryptography** — ML-KEM-1024 + X25519 hybrid key exchange
- **Triple-layer encryption** — ML-DSA-87 + Ed25519 signatures
- **Constant-time token comparison** to prevent timing attacks
- **Content Security Policy** headers on all dashboard responses
- **Bearer token authentication** for all API endpoints
- **Input validation** on all configuration updates
- **CORS restrictions** limited to same-origin by default
- **Blake3 keyed hashing** for warrant canary signatures
- **Automatic key rotation** at configurable intervals
- **Kill switch** to prevent traffic leaks on disconnect
- **Zero-log architecture** — no traffic, connection, or DNS logs stored
- **Memory zeroization** — sensitive keys wiped from memory after use

## Responsible Disclosure Timeline

1. Reporter sends vulnerability details via email
2. We acknowledge receipt within 48 hours
3. We investigate and develop a fix within 7 days
4. We release the fix and credit the reporter
5. Public disclosure after 30 days (or sooner if agreed)

---

# 🇳🇱 Beveiligingsbeleid

> *"Alleen een dwaas vertrouwt erop dat zijn tegenstander eerlijk speelt."* — Vegeta

## Een Kwetsbaarheid Melden

Als je een beveiligingskwetsbaarheid ontdekt in SaiyanShield, meld dit dan verantwoordelijk.

**Open GEEN publieke issue.**

Stuur in plaats daarvan een e-mail naar: **security@saiyanshield.dev**

Je ontvangt binnen 48 uur een reactie. We werken met je samen om het probleem te begrijpen en een fix te coördineren voordat er publieke bekendmaking plaatsvindt.

## Ondersteunde Versies

| Versie  | Ondersteund |
|---------|-------------|
| latest  | Ja          |

## Beveiligingsmaatregelen

SaiyanShield implementeert de volgende beveiligingsmaatregelen:

- **Post-quantum cryptografie** — ML-KEM-1024 + X25519 hybride sleuteluitwisseling
- **Drielaagse encryptie** — ML-DSA-87 + Ed25519 handtekeningen
- **Constante-tijd token vergelijking** om timing-aanvallen te voorkomen
- **Content Security Policy** headers op alle dashboard responses
- **Bearer token authenticatie** voor alle API endpoints
- **Invoervalidatie** op alle configuratie-updates
- **CORS beperkingen** standaard beperkt tot same-origin
- **Blake3 keyed hashing** voor warrant canary handtekeningen
- **Automatische sleutelrotatie** op instelbare intervallen
- **Kill switch** om verkeerslekken bij verbreken te voorkomen
- **Zero-log architectuur** — geen verkeers-, verbindings- of DNS-logboeken opgeslagen
- **Geheugen-zeroisatie** — gevoelige sleutels gewist uit geheugen na gebruik

## Verantwoorde Onthullingstijdlijn

1. Melder stuurt kwetsbaarheidsdetails via e-mail
2. Wij bevestigen ontvangst binnen 48 uur
3. Wij onderzoeken en ontwikkelen een fix binnen 7 dagen
4. Wij brengen de fix uit en vermelden de melder
5. Publieke onthulling na 30 dagen (of eerder indien overeengekomen)
