# EMA CORE (EMA)


**Status: deployed on Base Mainnet; source verified as an exact match on Blockscout. Not independently audited.**


EMA CORE is a fixed-supply, zero-tax ERC-20 core token developed by AssetDeploy LLC for the 0628DAO ecosystem and future autonomous AI-agent use.


## ThreeCore direction — EMA

EMA is the practicality- and sustainability-focused identity within ThreeCore.
The six-minute film illustrates decentralized prediction markets; the separate
120-second wallet special introduces one dedicated wallet per agent, backend
signing within authorized limits, settlement accounting and own-token buyback
and burn.

Dedicated-wallet coding is underway; the films do not establish a released
wallet, completed prediction-market integration or realized profits. Agent
decisions, trading, buybacks and liquidity operations require separate software.
x402 is not a prerequisite.

EMAは現実性・継続可能性重視。専用ウォレットは開発中で、
各自が分析・判断・実行し、実現収益を自トークンのBuyback & Burnへ
つなげる方向です。動画は完成済み機能や運用実績の証明ではありません。

Despite this repository's `-Draft` name, `contracts/EMACore.sol` is the
current token implementation described below. Root-level draft files are
historical references.

See [ThreeCore direction, wallet workflow and implementation boundaries](https://github.com/0628DAO/0628DAO-Protocol/blob/main/docs/THREECORE.md).

## Mainnet deployment


| Item | Value |
|---|---|
| Network | Base Mainnet (chain ID 8453) |
| Contract | [`0xBaE0933d509b83B7bbAb3AaB9feD413504382a76`](https://base.blockscout.com/address/0xBaE0933d509b83B7bbAb3AaB9feD413504382a76?tab=contract) |
| Deployment transaction | [`0x781f30ca91c974e60853d9dd1b8e71700bfd835eddffbd2b7222f0846f1208aa`](https://base.blockscout.com/tx/0x781f30ca91c974e60853d9dd1b8e71700bfd835eddffbd2b7222f0846f1208aa) |
| Initial holder | `0xfbE494B465efe6d0Daff80dC715302d0Fa0Ac5d9` |
| Initial supply | 777,000,000 EMA |
| Compiler | Solidity 0.8.34 |
| Optimizer / EVM | Disabled / default |
| Source verification | Blockscout exact match |
| Project page | [assetdeploy.xyz/#emacore](https://assetdeploy.xyz/#emacore) |


## Aerodrome liquidity

| Item | Value |
|---|---|
| DEX | Aerodrome Finance |
| Pool type | Volatile (vAMM) |
| Pair | EMA/USDC |
| Pool | [`0x8c0689EE10CF35A76149BA37808b5758C5826688`](https://base.blockscout.com/address/0x8c0689EE10CF35A76149BA37808b5758C5826688) |
| Initial liquidity | 7,770,000 EMA + 100 USDC |
| Add-liquidity transaction | [`0xb25899bd34b947786bc477705dc0342e5233a01ce42749291723961fec10edb0`](https://base.blockscout.com/tx/0xb25899bd34b947786bc477705dc0342e5233a01ce42749291723961fec10edb0) |
| USDC | [Canonical Base USDC](https://base.blockscout.com/address/0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913) |

This pool is external to the EMA token contract. Pool balances and price may change through trading and later liquidity changes.

## Confirmed token specification


| Item | Value |
|---|---|
| Contract | `EMACore` |
| Name | EMA CORE |
| Symbol | EMA |
| Decimals | 18 |
| Transfer / buy / sell tax | 0% |
| Additional minting | None |
| Burn | Holder burn and allowance-based `burnFrom`, as in DATCORE |
| Permit | EIP-2612, domain name `EMA CORE` |
| Owner / admin / pause / upgrade / proxy | None |


The entire supply was minted once to the initial-holder address. The contract contains no vesting, automatic distribution, price support, liquidity, blacklist, pause, upgrade, or administrator mint mechanism. Any liquidity position is external to the token contract.


## Base Sepolia reference


The same implementation was deployed and exact-match verified on Base Sepolia before mainnet release:


- Contract: [`0x20C3bb2548a1CE188229A6128dF0e9612259185E`](https://base-sepolia.blockscout.com/address/0x20C3bb2548a1CE188229A6128dF0e9612259185E?tab=contract)
- Network: Base Sepolia (chain ID 84532)


## Provenance and scope


Base source: [0628DAO/DAT](https://github.com/0628DAO/DAT/tree/0aa811b9c7607d7af6129a943cca8be72974a59b), `contracts/DATCore.sol`. Token logic is unchanged except for the contract/error names, token name, symbol, permit domain, and initial supply. DATCORE's MIT license and pinned OpenZeppelin/compiler dependencies are retained.


Prior Draft documentation is archived at [docs/legacy-draft-readme.md](docs/legacy-draft-readme.md). Existing token deployments are not migrated or converted by this contract.


## Local checks


Use Node.js 22 or newer:


```sh
npm ci
npm run check
```


The test suite covers metadata, supply, allocation, transfers, allowances, holder burns, authorized and unauthorized `burnFrom`, EIP-2612 permits, replay and expiry rejection, EIP-712 domain data, and the absence of privileged functions.

Passing local checks and explorer verification are not substitutes for an independent security audit. Never share keys, seed phrases, keystore passwords, or secret screenshots.

© AssetDeploy LLC. MIT License applies to the DATCORE-derived implementation.
