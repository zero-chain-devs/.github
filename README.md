<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=200&section=header&text=Zero%20Chain%20Devs&fontSize=60&fontColor=ffffff&fontAlignY=38&desc=Building%20the%20ZeroChain%20Ecosystem&descAlignY=58&descSize=20&animation=fadeIn" width="100%" />

<br/>

[![Org](https://img.shields.io/badge/Organization-zero--chain--devs-302b63?style=for-the-badge&logo=github&logoColor=white)](https://github.com/zero-chain-devs)
[![Blockchain](https://img.shields.io/badge/Blockchain-ZeroChain-24243e?style=for-the-badge&logo=bitcoin&logoColor=white)](#)
[![License](https://img.shields.io/badge/License-MIT-0f0c29?style=for-the-badge&logo=opensourceinitiative&logoColor=white)](LICENSE)

</div>

---

## ⛓️ What is ZeroChain?

**ZeroChain** is a next-generation blockchain with a **dual-account model** — combining the familiarity of EVM with the cryptographic power of native ed25519 accounts.

| Feature | Description |
|---|---|
| 🔐 **Dual Accounts** | `secp256k1 / EVM` + `ed25519 / Native` |
| ⚡ **Compute Transactions** | Native `zero_simulateComputeTx` / `zero_submitComputeTx` |
| 🌐 **Multi-Network** | `local` · `devnet` · `testnet` · `mainnet` |
| 🔍 **Full Explorer** | Etherscan-style block explorer |
| 📱 **Mobile Wallet** | Flutter hybrid wallet (iOS & Android) |

---

## 🚀 Projects

<div align="center">

### 🔭 [zero-explore](https://github.com/zero-chain-devs/zero-explore)

*An Etherscan-style block explorer for ZeroChain*

[![TypeScript](https://img.shields.io/badge/Frontend-TypeScript%20%2B%20React%20%2B%20Vite-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://github.com/zero-chain-devs/zero-explore)
[![Rust](https://img.shields.io/badge/Backend-Rust%20%2B%20Axum-CE422B?style=flat-square&logo=rust&logoColor=white)](https://github.com/zero-chain-devs/zero-explore)

</div>

```
zero-explore/
├── frontend/   # Vite + React — 实时区块浏览 UI
└── backend/    # Rust + Axum — ZeroChain RPC 代理与短缓存
```

<details>
<summary><b>✨ Feature Highlights</b></summary>

- 🏠 **Network Overview** — Chain stats, hashrate, gas price, coinbase
- 📦 **Block Explorer** — Block list, detail pages, range queries, pagination
- 📬 **Address Details** — EVM balance + Native UTXO via `zero_getAccount` / `zero_getUtxos`
- 🧮 **Compute Tx Lookup** — Query results via `zero_getComputeTxResult`
- 🔎 **Smart Search** — Unified search across block height, address, tx hash, object, output, domain
- 🔥 **Hot Addresses** — Usage-aggregated active address ranking
- 🔄 **Auto-refresh** — 5-second live homepage updates
- ⚡ **Backend Cache** — 5-second short-circuit cache reduces RPC pressure
- 🌡️ **Status Indicator** — Backend + node RPC health displayed in the top bar
- 🃏 **Dual View** — Field cards + Raw JSON on every detail page

</details>

---

<div align="center">

### 📱 [zero-wallet-mobile](https://github.com/zero-chain-devs/zero-wallet-mobile)

*A hybrid Flutter wallet for ZeroChain — EVM & Native accounts in one app*

[![Flutter](https://img.shields.io/badge/Flutter-Dart-02569B?style=flat-square&logo=flutter&logoColor=white)](https://github.com/zero-chain-devs/zero-wallet-mobile)
[![EVM](https://img.shields.io/badge/secp256k1-EVM%20%2F%20BIP39-627EEA?style=flat-square&logo=ethereum&logoColor=white)](#)
[![Native](https://img.shields.io/badge/ed25519-Native%20Compute-24243e?style=flat-square&logo=keybase&logoColor=white)](#)

</div>

```
lib/
├── core/           # 网络配置、RPC 客户端、主题、加密工具
├── data/models/    # 钱包数据模型
└── presentation/   # 页面 & 状态管理 (Provider)
```

<details>
<summary><b>✨ Feature Highlights</b></summary>

**Account Management**
- 🔑 Create / import `secp256k1` EVM wallet (BIP39 mnemonic, path `m/44'/60'/0'/0/0`)
- 🗝️ Create / import `ed25519` Native wallet (random private key)
- 🔄 Switch active account from the UI

**Security**
- 🔒 Local vault encryption: `PBKDF2-SHA256 (120,000 iter)` + `AES-256-GCM`
- 💾 Sensitive data stored in `flutter_secure_storage`
- 🚫 Mnemonics & private keys never leave the device

**Transactions**
- 💸 EVM: `eth_getBalance` + `eth_sendRawTransaction`
- ⚙️ Native: JSON compute → local sign → `zero_simulateComputeTx` / `zero_submitComputeTx`
- 🌐 Network switching: `local` / `devnet` / `testnet` / `mainnet` + custom RPC URL

</details>

---

## 🛠️ Tech Stack

<div align="center">

| Layer | Technology |
|---|---|
| 🔗 **Blockchain** | ZeroChain (secp256k1 · ed25519 · Compute RPC) |
| 🖥️ **Explorer Frontend** | TypeScript · React · Vite |
| ⚙️ **Explorer Backend** | Rust · Axum |
| 📱 **Mobile Wallet** | Flutter · Dart |
| 🔐 **Cryptography** | BIP39 · secp256k1 · ed25519 · PBKDF2 · AES-GCM |

</div>

---

## 🌐 Network Reference

| Network | Chain ID | EVM RPC | WS |
|---|---|---|---|
| `local` | 31337 | `http://127.0.0.1:8545` | `ws://127.0.0.1:8546` |
| `devnet` | 10088 | `http://127.0.0.1:28545` | `ws://127.0.0.1:28546` |
| `testnet` | 10087 | `http://127.0.0.1:18545` | `ws://127.0.0.1:18546` |
| `mainnet` | 10086 | `http://127.0.0.1:8545` | `ws://127.0.0.1:8546` |

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=100&section=footer" width="100%" />

*Building the ZeroChain ecosystem — one block at a time.*

</div>