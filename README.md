# 🕓 TVS CodeStamp v2 – Public Time-Based Signing Protocol

![TVS Banner](https://github.com/TimeVaultSecure/assets/blob/main/tvs_codestamp_banner.png)

TVS CodeStamp v2 is an open protocol and CLI toolset for creating and verifying public, cryptographically signed timestamps.

> ⚠️ This repository is a public proof-of-concept of how TVS anchors file hashes in time using transparent, verifiable, HMAC-based signatures.

---

## 🔐 What is CodeStamp?

A `TVS CodeStamp` looks like this:

```
2025-04-20T10:43:28.247634+00:00.9db761a6204b50bb38cfaaac1c6405fa05a1094d1559e69c6ce8c0a5471c3787
```

It includes:
- ISO8601 timestamp
- HMAC signature (SHA-256)
- daily rotating key (public via API)

You can verify the signature using the file hash, the timestamp, and the daily key – even offline.

---

## 🚀 Try It Now

```bash
python tvs_cli.py <sha256-hash> --datetime 2025-04-20T10:00:00Z
python tvs_cli.py <hash> --offline keys/2025-04-20.json
```

---

## 📘 Documentation

- [📄 Whitepaper](https://timevaultsecure.com/whitepaper/)
- [🛠 API Reference (coming soon)]()
- [📂 Example Certificates (PDF)](./examples/)

---

## 📡 Live Service

TVS Daily Key is published publicly every day at **09:00 UTC**:

```
https://timevaultsecure.com/api/daily-key/
```

You can also verify timestamps at:

```
https://timevaultsecure.com/verify/
```

---

## 📄 License

This project is licensed under the [MIT License](./LICENSE).

© 2025 TimeVaultSecure. All rights reserved.

---
