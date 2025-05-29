# Polynomic Vault — Shamir's Secret Sharing Scheme

Polynomic Vault is a Python implementation of **Shamir’s Secret Sharing Scheme (SSS)** — a cryptographic algorithm that splits a secret (like a private key) into multiple shares. Only a threshold number of those shares are required to reconstruct the original secret.

This is widely used for secure multi-party custody of sensitive information, such as blockchain private keys, passwords, or critical credentials.

---

## How It Works

- A secret is encoded as the constant term of a random polynomial.
- `n` shares are created by evaluating the polynomial at `n` distinct x-values.
- Only `k` out of `n` shares are needed to reconstruct the secret using **Lagrange Interpolation** over a finite field.

---

## Features

- Create secret shares with configurable threshold `k` and total shares `n`
- Reconstruct the secret using any `k` valid shares
- Operates over a large prime field (modular arithmetic)

---

## Requirements

- Python 3.x

No external libraries are required.

---
