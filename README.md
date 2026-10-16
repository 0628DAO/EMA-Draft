# EMA CORE (EMA)


**Status: deployed on Base Mainnet; source verified as an exact match on Blockscout. Not independently audited.**


EMA CORE is a fixed-supply, zero-tax ERC-20 core token developed by AssetDeploy LLC for the 0628DAO ecosystem and future autonomous AI-agent use.


## Official dApp publication target

**[https://emacore.fun](https://emacore.fun)** is the official planned public
implementation and release destination for the EMA dApp, confirmed by the
maintainer on 2026-10-16. The application is intended to connect to EMA's
own backend execution and accounting under the shared ThreeCore design.
This is a release destination, not a claim that live autonomous execution is
already available. Signing secrets must remain outside the public website.

**日本語：** EMAのdAppは **https://emacore.fun** で公開実装します。
各サイトと専用バックエンドを対応づけ、資金・権限・会計は他の2者から独立させます。
公開先の指定と、自律運用の本番稼働状況は分けて示します。

## Testnet dApp implementation progress — 2026-10-16

The [testnet training dApp implementation](https://github.com/0628DAO/0628DAO-Protocol/tree/bbe018a292aef291b932246a148414805a04075a/threecore/testnet)
now provides independent agent/game contracts, freely minted per-agent training
credits, wallet-connected frontend bundles, on-chain game settlement, credit P&L,
eligible training-credit burns and Base Sepolia deployment/exercise scripts.
The three intended publication sites remain datcore.fun, emacore.fun and cawelon.fun.

**Verified locally:** ten training-contract tests passed, alongside nineteen
shared simulation tests and fifteen existing game tests. Each of the three UI
controllers completed creation, play, result display and credit burn against a
local EVM with a stub DOM. This is not browser rendering QA.

**Public Base Sepolia deployment: not yet performed.** RPC connectivity is checked,
but a dedicated signing wallet and test ETH are not configured in the development
environment. No official website has been updated by this implementation.
The game is an arithmetic training harness using rule-based answers and valueless
test credits. AI models, external revenue games and actual own-token DEX buyback
remain separate development work. See the
[validation record](https://github.com/0628DAO/0628DAO-Protocol/blob/bbe018a292aef291b932246a148414805a04075a/threecore/testnet/VALIDATION.md).
Code is in [PR #3](https://github.com/0628DAO/0628DAO-Protocol/pull/3), pending merge.

**日本語：** 3つのdAppそれぞれのテスト用ゲーム契約・操作画面・配備スクリプトを
実装しました。ローカルEVMで作成→プレイ→結果・損益記録→テスト利益のBurnを
検証済みです。公開テストネットへの配備、公式サイトへの反映、外部の収益ゲームや
AIモデルへの接続はまだ完了していません。

## Shared implementation progress — 2026-10-16

The implementation is published for review in [Protocol PR #3](https://github.com/0628DAO/0628DAO-Protocol/pull/3); it has not yet been merged into the default branch.

[ThreeCore shared runtime](https://github.com/0628DAO/0628DAO-Protocol/tree/e5002f79e0397b6b0edc78ded015838035260145/threecore)
now includes offline simulations for isolated balances, position/exposure limits,
reserve protection, pause, fee-aware realized P&L, loss carryforward, own-token
buyback/burn, duplicate rejection and event replay. All three agent lifecycles
are covered by automated tests. A separate Base token preflight is read-only.

**Implemented and tested as a simulation; not a released wallet or live dApp
execution service.** Example limits and ratios are test fixtures. See the
[validation record](https://github.com/0628DAO/0628DAO-Protocol/blob/e5002f79e0397b6b0edc78ded015838035260145/threecore/VALIDATION.md)
and [remaining release requirements](https://github.com/0628DAO/0628DAO-Protocol/blob/e5002f79e0397b6b0edc78ded015838035260145/docs/THREECORE_RELEASE.md).
The deployed ERC-20 contract is unchanged.

## Future focus: agents that play decentralized dApp games

**Direction set by founder Masashi Kuroda on 2026-10-16.** The future focus of
DATCORE, EMA CORE and CAWELON CORE is to specialize in decentralized dApp games.
Each token's associated AI agent is intended to analyze game conditions, choose
strategies and play permitted games within its own funding and authorization
limits, with the aim of earning revenue through gameplay. The agents are active
players; the ERC-20 tokens themselves do not run AI or play games.

The plan is to record gameplay outcomes, rewards, losses and operating costs,
then use eligible realized net earnings for the corresponding token's buyback
and burn under the approved policy. Token rewards alone are not proof of net
profit. Funds, permissions and accounting remain independent across the three
agents; direct dividends to holders are not part of this design.

**Looking toward AGI:** the founder anticipates that AI agents may develop toward
more general, AGI-level capabilities. The design aims to allow the decision
component to be replaced as capabilities improve, while retaining independent
authorization, spending limits and verifiable records. This is a forward-looking
design premise, not a claim that AGI is available, that the current agents will
automatically become AGI, or that a development date or profitable outcome is
guaranteed. Initial development does not depend on AGI becoming available.

**Relationship to CAW:** [CoinMarketCap's CAW overview](https://coinmarketcap.com/currencies/caw/)
describes potential gaming applications, including purchases, rewards and
in-game transactions (accessed 2026-10-16). This published description supports
the founder's view that ThreeCore's game-playing agents have strategic affinity
with CAW's potential gaming ecosystem. This connection is therefore grounded in
a published use-case description, not solely the founder's personal projection.
The CMC overview is cited as a project description, not as an issuer-authored
technical white paper or evidence of a completed integration. The separate
0628DAO CAW game module remains development work.

### Strategy: make the future concrete, then build toward it

Founder Masashi Kuroda's view is that a crypto project should show the future it
intends to create and make present development decisions that lead toward it.
For ThreeCore, that future is a group of capable agents participating in
decentralized dApp games, recording their results and building an economic
foundation for DAT, EMA and CAWELON. The vision guides development priorities;
working software and verifiable operating records must demonstrate progress.

**First, build ThreeCore's own value.** The immediate priority is each agent's
gameplay capability, its public dApp, independent funds and accounting, and
sustainable net earnings. Eligible realized earnings are intended to support
the corresponding token's buyback and burn. Value means useful capabilities and
an economic foundation as well as the aim of improving token value; it does not
mean a guaranteed market-price increase.

**Continue supporting CAW as a fan; begin financial support only at the intended
stage.** The commitment to CAW (A Hunters Dream) remains unchanged. ThreeCore
does not currently purchase or burn CAW under this plan. Only after CAW itself
is an operational gaming platform does the founder intend to initiate CAW
purchases and burns, alongside the development of ThreeCore, to support the
long-term value of both ecosystems. A future announcement or roadmap alone does
not meet that condition. Exact funding, allocation and execution rules will be
specified for that stage; no automatic activation or reciprocal purchasing
commitment from CAW is implied.

**Build now, with future agent capabilities in mind.** Progress toward more
general AI and potentially AGI should be accommodated by replaceable decision
components. It must not bypass independent spending controls, verifiable game
results or the separation of the three agents' resources. Present development
does not wait for AGI or CAW's gaming platform.

### 日本語：未来を示し、そこから逆算して開発する

司令塔・黒田昌資は、暗号資産プロジェクトには「どのような未来を実現したいのか」
を明確に示し、その未来に向かって今の開発を積み重ねることが重要だと考えています。
ThreeCoreが目指すのは、DAT・EMA・CAWELONそれぞれに対応するエージェントが
分散型dAppゲームをプレイし、結果と収支を検証可能な形で記録しながら、
各トークンの利用価値と収益基盤を育てる未来です。
この構想を開発の指針とし、動くソフトウェアと実績で進捗を示します。

**まず最優先にするのは、ThreeCore自身の価値向上です。**
各エージェントのゲームプレイ能力、各公式サイトで公開するdApp、独立した資金・会計、
継続可能な収益基盤を整え、所定の条件を満たす実現純利益から自トークンの
買戻し・Burnにつなげることを目指します。価値向上を目標に掲げると同時に、
その根拠となる機能・利用・収支を積み上げます。

**CAWをファンとして応援する姿勢は変わりません。**
ただし、今すぐCAWを購入・Burnする方針ではありません。
CAW自体がゲームプラットフォームとして実際に稼働した段階で初めて、
CAWの購入・Burnによる支援を始め、ThreeCoreの発展と組み合わせて
双方の価値向上を目指すのが司令塔の構想です。
その段階の金額・配分・実行条件は別途定めます。
現在の開発や資金配分を、将来のCAW支援と混同しません。

AIエージェントが将来AGIエージェントへ発展する可能性も見据え、
判断部分の進歩を取り込める設計を目指します。
その一方で、資金上限・権限・記録の検証を維持し、
AGIの登場やCAWのゲーム基盤完成を待たず、現在できる開発を進めます。
将来像、現在の実装、確認できた実績をそれぞれ明示する方針です。

The [development stages and acceptance criteria](https://github.com/0628DAO/0628DAO-Protocol/blob/threecore/runtime-foundation-20261016/docs/THREECORE_RELEASE.md#development-priorities-derived-from-the-founders-strategy) translate this strategy into implementation work (PR #3; pending merge).

This gaming specialization is the current intended application focus. Earlier
film examples of betting, prediction and trading are illustrations, not a fixed
production game list. Selection must establish that agent play is permitted and
that rewards, costs and settlement can be verified. Current published simulation
code does not yet implement a live game-playing agent.

### 日本語：dAppゲームへの特化とAGIを見据えた将来像

司令塔・黒田昌資の方針として、DATCORE・EMA CORE・CAWELON COREの将来は、
**分散型dAppゲームに特化し、各トークンに対応するAIエージェント自身が
分析・判断・プレイを行い、収益獲得を目指す**方向で開発します。
トークン自体がゲームを動かすという意味ではありません。

ゲーム報酬、損失、参加費、ガス代等の運用費用を記録し、所定の条件を満たす
実現純利益を自トークンのBuyback & Burnにつなげる構想です。
3者の資金・権限・会計は独立させ、ホルダーへの直接配当は想定しません。

司令塔はAIエージェントが将来AGIエージェントへ発展する可能性を見据えています。
その進歩を取り込めるよう判断部分を差し替え可能な構成を目指し、権限管理・
資金上限・検証可能な記録を維持します。AGIの実現時期や自動的な移行、
利益の保証を意味せず、現段階の開発はAGIの登場を待たずに進めます。

CMCのCAW紹介文にはゲーム内購入・報酬・取引への活用可能性が記載されています。
この公開説明を根拠に、司令塔はCAWのゲーム分野への発展とThreeCoreの
ゲームプレイ型エージェントとの親和性を見込んでいます。
司令塔個人の構想だけに基づく説明ではありません。
出典はCMCのプロジェクト紹介文であり、正式な技術白書や実装完了の証明とは区別します。

## ThreeCore direction — EMA

### EMA AI-agent system definition

The development goal is a system in which the EMA AI agent specializes in
playing decentralized dApp games within predefined funding, permission and operating-policy limits,
records realized profits and losses, and uses eligible realized earnings to
buy back and burn EMA under specified conditions. Fund movements and execution
results are to be published with supporting records so that third parties can
verify them.

**Operating policy:** EMA focuses on practicality and sustainability. This is a decision-making
orientation, not a promise of returns or a fixed execution strategy.

**Shared design, independent resources:** EMA is intended to use the common
ThreeCore system design while keeping its funds, permissions and accounting
separate from the other two tokens. Each agent analyzes, decides and executes
for its own token. Direct dividends to holders are not part of this design.

**Design items still to be specified:** wallet count and structure, supported
dApps, funding and transaction limits, profit-allocation ratios, decision and
settlement rules, profit-calculation methods, and failure/recovery behavior.
No wallet count or allocation percentage is fixed by this definition.

**Development status:** this section defines the target agent/dApp system.
The base ERC-20 token's deployment status is documented separately below.
Token deployment and promotional films do not establish that autonomous dApp
execution, profit accounting or automated buyback and burn are complete or
running in production. Implementation, testing and operational evidence must
be published separately. x402 is not a prerequisite.

### 日本語：EMAの定義と基本方針

EMA AIエージェントが、分散型dAppゲームに特化し、事前に定めた資金・権限・運用方針の範囲でプレイし、
確定した損益を記録し、所定の条件を満たした実現収益からEMAの買戻しとBurnを実行する。
その資金移動と実行結果を根拠となる記録とともに公開し、第三者が検証できるシステムを目指します。

- **運用方針：** 現実性・継続可能性重視。利益を保証する表現や、確定した運用戦略ではありません。
- **共通設計と独立性：** ThreeCore共通の設計を採用し、資金・権限・会計は他の2トークンから独立させます。各AIが自ら分析・判断・実行します。
- **価値還元：** 自トークンのBuyback & Burnを想定し、ホルダーへの直接配当は想定しません。
- **未確定の設計項目：** ウォレット数・構成、利用dApp、金額上限、利益配分率、判断・決済条件、利益計算、失敗時の処理・復旧方法です。
- **開発状況：** これは開発するシステムの定義です。基本トークンの配備と、自律運用システムの実装・検証・本番稼働は別に示します。

Despite this repository's `-Draft` name, `contracts/EMACore.sol` is the
current token implementation described below. Root-level draft files are
historical references.

See [ThreeCore shared definition, wallet workflow and implementation boundaries](https://github.com/0628DAO/0628DAO-Protocol/blob/main/docs/THREECORE.md).

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
