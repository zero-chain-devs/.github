# ZeroChain

ZeroChain 是一条以 **Native UTXO Compute** 为主线、以 **PoW** 为安全基座的区块链网络（当前为 **Native-Only** 形态）。

## 关键特性

- **UTXO Compute**：统一执行、状态与资源表达
- **ed25519** 原生签名（规范地址：`ZER0x...`，20 bytes）
- **PoW** 共识与挖矿接口：`zero_getWork` / `zero_submitWork`
- **HTTP JSON-RPC + WebSocket**：`web3_*` / `net_*` / `zero_*`

## Canonical RPC

- 模拟：`zero_simulateComputeTx`
- 写入：`zero_submitComputeTx`
- 结果：`zero_getComputeTxResult`
- Domain/对象/输出：`zero_getDomain` / `zero_getObject` / `zero_getOutput`
- 账户/UTXO：`zero_getAccount` / `zero_getUtxos`
- 区块/挖矿：`zero_getLatestBlock` / `zero_getWork` / `zero_submitWork`
- WebSocket：`zero_subscribe` / `zero_unsubscribe`

## 网络参数（默认）

| network | chain_id / network_id | HTTP JSON-RPC | WebSocket |
|---|---:|---|---|
| `local` | 31337 | `http://127.0.0.1:8545` | `ws://127.0.0.1:8546` |
| `devnet` | 10088 | `http://127.0.0.1:28545` | `ws://127.0.0.1:28546` |
| `testnet` | 10087 | `http://127.0.0.1:18545` | `ws://127.0.0.1:18546` |
| `mainnet` | 10086 | `http://127.0.0.1:8545` | `ws://127.0.0.1:8546` |

> 说明：部分本地 E2E/CI 脚本会覆写端口（例如 `19545/19546`）。

## 经济参数（与节点一致）

- 目标出块时间：10 秒
- 初始区块奖励：5 ZC
- 减半周期：2,100,000 blocks（约 243.06 天）
- 奖励地板：无（持续减半）
- 理论最大供应量：约 21,000,000 ZC

## 生态项目

- `zero-chain`：节点、共识、P2P、Compute、RPC、CLI
- `zero-mining-stack`：矿池 + 矿工（MVP）
- `zero-explore`：区块浏览器（前后端一体）
- `zero-wallet-chrome`：浏览器插件钱包（native-only）
- `zero-wallet-mobile`：Flutter 钱包（native-only）

## 关于本仓库

`zero-chain-devs/.github` 用于存放组织级 GitHub 配置与 Profile 页面内容（见 `profile/README.md`）。
