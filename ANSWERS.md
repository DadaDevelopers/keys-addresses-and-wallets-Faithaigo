
### 1. Difference Between Hardened and Non-Hardened Keys

- **Non-Hardened Keys**:
  - Child public keys can be derived from the parent public key alone.
  - Allows generating public addresses without exposing private keys.
  - Risk: If a child private key and parent public key are exposed, other sibling keys can be compromised.

- **Hardened Keys**:
  - Child keys require the parent private key to be derived.
  - More secure: a leaked child key does not compromise other keys.
  - Limitation: cannot generate addresses from the parent public key alone.


### 2. Why Wallet Developers Prefer Deterministic Wallets

- **Deterministic (HD) Wallets**:
  - All keys are generated from a single seed (mnemonic phrase).
  - One backup restores all addresses and keys.
  - Supports hierarchical organization of accounts: Organized accounts and addresses via standardized paths (BIP44).
  - Allows generating billions of addresses from one seed.

- **Non-Deterministic Wallets**:
  - Keys are generated randomly and independently.
  - Each key must be backed up individually.
  - Risk of losing keys is higher.

**These are the benefits of Deterministic Wallets for Developers**:
1. Easy backup & recovery.
2. Better organization and account management.
3. Enhanced privacy through new addresses per transaction.
4. Lower risk of losing funds due to lost keys.
