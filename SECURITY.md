# Security Policy

## Security Architecture

- **Local-First Data:** Cards, media references, and settings are stored strictly on the user's device. PanoRA does not collect behavioral analytics or upload user content to cloud servers.
- **Vault Encryption:** When enabled, the local vault encrypts data with AES-256-GCM using keys derived via `scrypt`. Encryption keys are dropped from memory upon lock.
- **LAN Transfers:** Pano Mesh uses authenticated encryption between paired devices on the local network; AirBridge uses ephemeral per-session 128-bit tokens and hides host-shared items while the vault is locked.
- **Offline License Verification:** License certificates are verified locally against an embedded Ed25519 public key.

## Reporting a Vulnerability

Please do not open public GitHub issues for security vulnerabilities. Report them privately to:

- Email: `security@uplif.app`

Include steps to reproduce, affected OS/version, and impact details. We acknowledge reports within 48 hours and coordinate disclosure once a fix is verified.
