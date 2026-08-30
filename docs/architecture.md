# Architecture

This document explains the Ciforus architecture at a high level.

It intentionally avoids private implementation details, internal infrastructure maps, secret operational procedures, and attack-surface specifics.

## Architecture Thesis

Ciforus is designed as a connected privacy system rather than a collection of isolated tools.

At a conceptual level, the platform combines:

- communication modules
- encrypted storage and notes
- wallet identity
- account security and recovery controls
- crypto-native payment workflows
- token utility integration

## High-Level Layer Model

The public Ciforus security narrative can be understood across three broad layers:

1. transport and delivery security
2. payload and content protection
3. identity, authorization, and recovery hardening

The reason for this layered model is simple: privacy fails when one layer is strong but another layer is weak.

Strong content encryption is not enough if identity recovery is weak. Strong transport security is not enough if private content is indexed broadly. Strong wallet identity is not enough if session handling is poorly protected.

## Module Relationship

The Ciforus product modules reinforce one another:

- Email provides private communication and premium identity.
- Wallet Messaging provides wallet-native communication.
- Storage protects sensitive files.
- Notes protect sensitive written material.
- Wallet Identity provides a trust layer.
- Pay Links extend the platform into crypto-native payment requests.
- Security Center protects access and recovery.

## Identity Layer

Wallet identity is a major architectural concept in Ciforus.

The platform is designed to use verified wallet ownership as a trust signal without turning wallet identity into a public exposure layer.

This supports:

- wallet-to-wallet communication
- verified interaction
- payment workflows
- account security flows
- tier-based wallet limits

## Email Boundary

Ciforus treats email as a distinct and sensitive trust domain.

The public architecture narrative describes email as operating through a secured backend and gateway-mediated model, rather than exposing raw mailbox operations directly through the user-facing surface.

Important distinction:

- Ciforus-to-Ciforus paths can support the strongest internal encryption guarantees.
- External email interoperability depends on standards-compatible transport and delivery behavior.

## Storage and Notes Boundary

Storage and Notes are positioned around confidentiality-first handling.

Public product direction includes:

- encrypted storage
- zero-knowledge principles
- per-file protection direction
- controlled sharing
- avoidance of broad server-side indexing of private content

## Search and Indexing Tradeoff

Ciforus intentionally avoids broad server-side full-text indexing of private message bodies, note content, and file content.

This is a deliberate privacy tradeoff.

Broad server-side search often requires readable indexes. Readable indexes can create privacy exposure. Ciforus prioritizes stronger privacy boundaries over convenience-first indexing.

## Token Integration Model

The token integration model is best understood as a hybrid on-chain plus in-app utility model.

On-chain:

- CIFORUS exists as an ERC-20 token on Ethereum mainnet.
- balances, transfers, and contract state are publicly reviewable.

Inside the app:

- utility can be expressed through billing recognition
- subscription discounts
- tier upgrades
- voluntary staking and product benefits
- account-bound presale ownership and eligible external claims
- rewards
- Pay Link and payment flows
- feature and entitlement logic

Not every product interaction needs to happen directly on-chain. The value-bearing token remains on-chain, while the product can recognize and apply utility through controlled application logic.

## Disclosure Boundary

This repository does not publish:

- private source code
- deployment secrets
- infrastructure topology
- internal operational procedures
- full implementation-level security details
- attack-surface specifics

## Summary

Ciforus architecture is designed around a connected privacy model: identity, access, communication, storage, notes, recovery, payments, and token utility are treated as parts of one ecosystem rather than separate surfaces.
