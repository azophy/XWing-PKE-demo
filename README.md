# X-Wing + XChaCha20-Poly1305 Demo

A minimal browser-based demo for post-quantum hybrid encryption using X-Wing (ML-KEM-768 + X25519) and XChaCha20-Poly1305.

## Why Hybrid?

X-Wing combines ML-KEM-768 (post-quantum) with X25519 (classical) — if either algorithm gets broken, your data stays safe.

## Usage

Open `index.html` in a browser. No build step required.

1. Click **Generate New Keypair**
2. Type a message in **Plain Text**
3. Click **Encrypt →** to encrypt
4. Click **← Decrypt** to decrypt

## Dependencies

Loaded via ESM from [esm.sh](https://esm.sh):

- [@noble/post-quantum](https://github.com/paulmillr/noble-post-quantum) — X-Wing KEM
- [@noble/ciphers](https://github.com/paulmillr/noble-ciphers) — XChaCha20-Poly1305
- [MVP.css](https://andybrewer.github.io/mvp) — Minimum page styling

## Wire Format

The encrypted output is packed as: `kemCipherText (1120 bytes) || nonce (24 bytes) || ciphertext + tag`

## License

MIT
