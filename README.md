# Shamir's Secret Sharing

[![license](https://img.shields.io/badge/license-AGPL_v3-blue?style=flat-square)](LICENSE)

A user-friendly web/GUI for Shamir’s Secret Sharing (SSS),
optimized for Bitcoin and BIP-39 mnemonics. Allow users to split BIP-39
mnemonics into `M`-of-`N` shards using the **SLIP-39 standard**.
The goal is to be the best UX for key backups.

[See the roadmap](./docs/ROADMAP.md).

<details><summary><h2>Contents</h2></summary>

<!-- toc -->

- [Problem](#problem)
- [Solution](#solution)

<!-- tocstop -->

</details>

## Problem

A single mnemonic seed phrase is a single point of failure.
Multisig (multiple keys) solves this, but it creates technical overhead like
managing multiple hardware wallets and coordination software.
There is not an accessible, user-friendly tool for
distributing the risk of a single seed phrase without incurring
the complexity of multisig.


## Solution

A browser-based, "single-file" GUI that allows users to split BIP-39 mnemonics
into `M`-of-`N` shards using the SLIP-39 standard.
Users can perform key ceremonies on air-gapped, amnesic hardware
(like a Tails USB on a non-networked Raspberry Pi) without needing a
command line.

