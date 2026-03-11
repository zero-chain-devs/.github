<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=200&section=header&text=Zero%20Chain%20Devs&fontSize=60&fontColor=ffffff&fontAlignY=38&desc=Building%20the%20ZeroChain%20Ecosystem&descAlignY=58&descSize=20&animation=fadeIn" width="100%" />

<br/>

[![Org](https://img.shields.io/badge/Organization-zero--chain--devs-302b63?style=for-the-badge&logo=github&logoColor=white)](https://github.com/zero-chain-devs)
[![Blockchain](https://img.shields.io/badge/Blockchain-ZeroChain-24243e?style=for-the-badge&logo=bitcoin&logoColor=white)](#)
[![License](https://img.shields.io/badge/License-MIT-0f0c29?style=for-the-badge&logo=opensourceinitiative&logoColor=white)](../LICENSE)

</div>

---

## ⛓️ What is ZeroChain?

**ZeroChain** is a **PoW** blockchain focused on **Native UTXO Compute** execution.
It uses **ed25519 native accounts** with canonical `ZER0x...` addresses, and exposes a `web3_* / net_* / zero_*` JSON-RPC + WebSocket surface.

| Feature | Description |
|---|---|
| 🔐 **Native Accounts** | `ed25519` signatures · canonical address `ZER0x...` (20 bytes) |
| ⚙️ **UTXO Compute** | `zero_simulateComputeTx` / `zero_submitComputeTx` / `zero_getComputeTxResult` |
| ⛏️ **PoW Mining** | `zero_getWork` / `zero_submitWork` |
| 🌐 **Network Profiles** | `local` · `devnet` · `testnet` · `mainnet` |
| 🔍 **Explorer** | Etherscan-style explorer (blocks / txs / compute / objects / outputs) |
| 👛 **Wallets** | Chrome extension + Flutter mobile wallet (Native-Only) |

---

## 🚀 Projects

<div align="center">

### 🧱 [zero-chain](https://github.com/zero-chain-devs/zero-chain)

*ZeroChain node + RPC + CLI (Native UTXO Compute · PoW · ed25519)*

[![Rust](https://img.shields.io/badge/Rust-Protocol%20%2B%20Node-CE422B?style=flat-square&logo=rust&logoColor=white)](https://github.com/zero-chain-devs/zero-chain)

</div>

---

<div align="center">

### ⛏️ [zero-mining-stack](https://github.com/zero-chain-devs/zero-mining-stack)

*Mining stack (pool + miner) for ZeroChain — MVP*

[![Rust](https://img.shields.io/badge/Rust-Pool%20%2B%20Miner-CE422B?style=flat-square&logo=rust&logoColor=white)](https://github.com/zero-chain-devs/zero-mining-stack)

</div>

---

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

- 🏠 **Network Overview** — Chain stats, hashrate, block interval, coinbase
- 📦 **Block Explorer** — Block list, detail pages, range queries, pagination
- 📬 **Address Details** — Native account + UTXO via `zero_getAccount` / `zero_getUtxos`
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

### 🧩 [zero-wallet-chrome](https://github.com/zero-chain-devs/zero-wallet-chrome)

*ZeroChain official browser extension wallet (Native-Only)*

[![TypeScript](https://img.shields.io/badge/TypeScript-Extension%20Wallet-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://github.com/zero-chain-devs/zero-wallet-chrome)
[![React](https://img.shields.io/badge/React-UI-61DAFB?style=flat-square&logo=react&logoColor=000000)](https://github.com/zero-chain-devs/zero-wallet-chrome)
[![Vite](https://img.shields.io/badge/Vite-Build-646CFF?style=flat-square&logo=vite&logoColor=white)](https://github.com/zero-chain-devs/zero-wallet-chrome)

</div>

---

<div align="center">

### 📱 [zero-wallet-mobile](https://github.com/zero-chain-devs/zero-wallet-mobile)

*A Flutter wallet for ZeroChain — Native-Only (ed25519)*

[![Flutter](https://img.shields.io/badge/Flutter-Dart-02569B?style=flat-square&logo=flutter&logoColor=white)](https://github.com/zero-chain-devs/zero-wallet-mobile)
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
- 🗝️ Create / import `ed25519` native accounts (canonical `ZER0x...` address)
- 🔄 Manage & switch active account from the UI

**Security**
- 🔒 Local vault encryption: `PBKDF2-SHA256 (120,000 iter)` + `AES-256-GCM`
- 💾 Sensitive data stored in `flutter_secure_storage`
- 🚫 Mnemonics & private keys never leave the device

**Transactions**
- ⚙️ Native compute: JSON → local sign → `zero_simulateComputeTx` / `zero_submitComputeTx`
- 🌐 Network switching: `local` / `devnet` / `testnet` / `mainnet` + custom RPC URL

</details>

---

## 🛠️ Tech Stack

<div align="center">

| Layer | Technology |
|---|---|
| 🔗 **Blockchain** | ZeroChain (Native UTXO Compute · ed25519 · PoW · JSON-RPC/WS) |
| 🔭 **Explorer** | TypeScript · React · Vite + Rust · Axum |
| 👛 **Wallets** | TypeScript · React · Vite + Flutter · Dart |
| ⛏️ **Mining Stack** | Rust |
| 🔐 **Cryptography** | ed25519 · PBKDF2 · AES-GCM |

</div>

---

## 🌐 Network Reference

| Network | Chain ID | HTTP JSON-RPC | WS |
|---|---:|---|---|
| `local` | 31337 | `http://127.0.0.1:8545` | `ws://127.0.0.1:8546` |
| `devnet` | 10088 | `http://127.0.0.1:28545` | `ws://127.0.0.1:28546` |
| `testnet` | 10087 | `http://127.0.0.1:18545` | `ws://127.0.0.1:18546` |
| `mainnet` | 10086 | `http://127.0.0.1:8545` | `ws://127.0.0.1:8546` |

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=100&section=footer" width="100%" />

*Building the ZeroChain ecosystem — one block at a time.*

</div>
