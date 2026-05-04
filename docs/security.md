# Security

Ciforus is positioned as a privacy-first platform with security and recovery controls built into the product foundation.

This document summarizes the public security philosophy at a safe abstraction level. It does not disclose sensitive internal implementation details.

## Security Philosophy

Ciforus treats privacy and security as system properties.

The product direction emphasizes:

- multi-layer encryption architecture
- end-to-end encryption direction across native communication paths
- zero-knowledge principles
- user-controlled access
- encrypted-by-default handling
- identity and recovery hardening
- careful boundaries around search and indexing

## Privacy as Infrastructure

Ciforus is built around the idea that privacy should not be added after the fact.

Private communication, file storage, notes, wallet identity, recovery, and payment behavior all affect the user's real privacy position. The platform therefore treats privacy as an ecosystem-level concern.

## End-to-End Encryption Boundary

Ciforus-to-Ciforus communication paths are where internal encryption guarantees apply most directly.

External email providers do not natively process Ciforus-specific encrypted payloads, so cross-provider email uses standards-compatible transport and delivery behavior rather than the same internal Ciforus-native guarantees.

This distinction is important because it avoids overclaiming.

## Zero-Knowledge Principles

The public Ciforus security narrative uses zero-knowledge principles to describe a design direction where infrastructure should minimize access to readable private content.

This includes:

- processing encrypted payloads where applicable
- reducing backend readability
- keeping sensitive content protected across storage and handling flows
- avoiding broad server-side indexing of private content
- tying access to user authorization and identity boundaries

## Key and Recovery Direction

Ciforus emphasizes user-controlled access and recovery hardening.

Public product direction includes:

- two-factor authentication using TOTP
- recovery email setup and verification
- 12-word recovery phrase direction
- BIP39-based recovery reinforcement
- wallet verification
- session management
- account-level defense workflows

The recovery model is framed around user control and hardened authorization, not casual plaintext recovery storage.

## Storage Security

Ciforus Storage is positioned around confidentiality-first encrypted file handling.

Public product direction includes:

- encrypted file storage
- zero-knowledge file protection principles
- secure sharing between verified Ciforus users
- privacy boundaries around file contents and metadata

## Notes Security

Ciforus Notes is positioned as an encrypted private workspace for sensitive writing.

The product direction avoids broad server-side indexing of private note content because readable indexes can undermine privacy boundaries.

## Wallet Identity Security

Wallet verification is used as a trust layer.

The purpose is not public exposure. The purpose is to connect cryptographic ownership with private interaction, messaging, Pay Links, and account controls.

## Security Limitations and Risk

No software system should be described as risk-free.

Relevant risk categories include:

- software bugs
- infrastructure configuration mistakes
- wallet and key management errors by users
- phishing or impersonation attempts
- smart contract and integration risk
- market and liquidity risk related to token behavior
- evolving regulatory treatment of crypto assets

Ciforus is designed to reduce exposure, but users remain responsible for wallet safety, recovery material, device hygiene, and phishing awareness.

## What Is Not Published Here

This repository does not publish:

- internal infrastructure maps
- private security procedures
- operational secrets
- key management internals
- attack-surface specifics
- private source code

## Summary

Ciforus security positioning is based on layered privacy, careful identity handling, encrypted product surfaces, account recovery discipline, and public transparency without unsafe disclosure.
