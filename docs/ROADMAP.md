# Roadmap

## 1 &mdash; BIP-39 & SLIP-39 Integration

Adapt
[@substrate-system/shamirs-secret-sharing](https://github.com/substrate-system/shamirs-secret-sharing)
to support BIP-39 12/24-word seeds. The tool will convert mnemonics to entropy,
shard the entropy, and optionally encode the resulting shares back into
mnemonic format **(SLIP-39)**, for easy physical backup.

## 2 &mdash; Progressive Web App

Create a minimal web tool that uses 
[@substrate-system/shamirs-secret-sharing](https://github.com/substrate-system/shamirs-secret-sharing)
to create key shards. This can be a purely frontend app &mdash; we don't need
to store any data. It should be installable as a
[PWA](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps), and
include an "offline check" that will warn the user if they are connected
to the internet while handling keys, and potentially block shard generation
unless offline.


## 3 &mdash; Feature &mdash; Paper Keys

Implement browser-side PDF generation for printable key shards with
SLIP-39 mnemonic, some metadata (eg, "shard 2  of 3"), and a QR code
(base45 encoding).


## 4 &mdash; Docs

Write clear documents for obtaining your secret key, and then splitting it into
shards via Shamir's Secret Sharing, and distributing the shards to
secure locations. Document how to do a recovery ceremony, in the event of
losing a private key, provide comprehensive docs about using the tool on
an "air-gapped" machine. Document how to verify the tool's hash and how to
run it on an air-gapped machine.
