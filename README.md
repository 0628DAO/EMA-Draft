# EMA CORE (EMA) — Base Sepolia Preparation

**Status: implementation prepared; not deployed; unaudited.**

This branch prepares the user-approved token on Base Sepolia (chain ID 84532),
using the DATCORE base-token design. No mainnet deployment, liquidity position,
holder migration, or production AI service is created by this branch.

## Confirmed token specification

| Item | Value |
|---|---|
| Contract | `EMACore` |
| Name | EMA CORE |
| Symbol | EMA |
| Initial supply | 777,000,000 EMA |
| Decimals | 18 |
| Transfer / buy / sell tax | 0% |
| Additional minting | None |
| Burn | Holder burn and allowance-based burnFrom, as in DATCORE |
| Permit | EIP-2612, domain name "EMA CORE" |
| Owner / admin / pause / upgrade / proxy | None |
| Initial recipient | Must be explicitly confirmed before deployment |

The entire supply is minted once to the constructor's initial-holder address.
No vesting, automatic distribution, price support, or liquidity is built in.
Approving an allowance permits the spender to use transferFrom **or burnFrom**.
This is an intentional DATCORE-aligned change from the legacy holder-burn-only
Draft. The root-level old Draft source remains preserved for reference;
Hardhat compiles only the new `contracts/` directory.

## Provenance and scope

Base source: [0628DAO/DAT](https://github.com/0628DAO/DAT/tree/0aa811b9c7607d7af6129a943cca8be72974a59b),
`contracts/DATCore.sol`. Token logic is unchanged except for the contract/error
names, token name, symbol, permit domain, and initial supply. DATCORE's MIT
license and its pinned OpenZeppelin / compiler dependencies are retained.

Prior Draft documentation is archived at [docs/legacy-draft-readme.md](docs/legacy-draft-readme.md).
Its old network / token details are historical; the table above governs this branch.
Existing deployed tokens remain unchanged. No migration entitlements, cutoff,
conversion ratio, or distributions are decided or executed here.

AI-agent risk profiles and decision-making logic are a separate future layer.
Changing token supply does not implement an aggressive or conservative AI,
guarantee returns, or reduce investment risk.

## Local checks (no wallet and no network transactions)

Use Node.js 22 or newer, and npm:

```sh
npm ci
npm run check
```

The suite tests metadata, supply, allocation, transfers, allowances, holder
burns, authorized and unauthorized burnFrom, EIP-2612 permits, replay and
expiry rejection, EIP-712 domain data, and the absence of privileged functions.
Passing local checks is not an independent security audit or mainnet approval.

## Separately approved Base Sepolia deployment

Use a dedicated testnet wallet; never reuse production keys. Confirm the
initial-holder public address and explicit authorization before deployment.
Set RPC and the test-only private key interactively in Hardhat's encrypted keystore:

```sh
npx hardhat keystore set BASE_SEPOLIA_RPC_URL
npx hardhat keystore set BASE_SEPOLIA_PRIVATE_KEY
```

Only after approval, set `INITIAL_HOLDER` to that confirmed public address and
`DEPLOY_APPROVAL=BASE_SEPOLIA_TEST_ONLY` in your shell; then run
`npm run deploy:base-sepolia`. Environment syntax depends on the shell.
The script rejects other chain IDs and invalid or zero recipients, then checks
bytecode, supply, and allocation. It creates an on-chain transaction if run.
No mainnet deployment command is included. Testnet tokens have no monetary value.

Never share keys, seed phrases, keystore passwords, or secret screenshots.

© AssetDeploy LLC. MIT License applies to the new DATCORE-derived implementation.

