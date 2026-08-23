README.md


EMADATA (EMA) — Provisional Relaunch Draft
Status: Draft / Not audited / Not deployed
Intended network: Arbitrum One
Maintainer: 0628DAO

EMADATA（EMA）の将来の再始動に向けた、新規ERC-20スマートコントラクトとdApp構成の暫定公開資料です。EMAは、0628DAOエコシステムにおける 0628BET（Prediction Layer／予測市場） の基盤トークンとして設計を進めています。

このリポジトリは、デプロイ前の設計・検証過程を透明化するために公開しています。現在掲載しているコードは監査前のドラフトであり、稼働中の新EMAや販売中の商品を示すものではありません。

固有仕様
項目	内容
Token Name	EMADATA
Symbol	EMA
Network	Arbitrum One
規格	ERC-20
初期発行量	777,000,000 EMA
Decimals	18
Transfer / Buy / Sell TAX	0%
Rewards / Reflection	なし
追加Mint	なし
Burn	保有者本人による自己Burnのみ
Permit	EIP-2612対応
Owner / Admin / Pause / Upgrade / Proxy	なし
既存EMAとの関係
既存EMAの参照コントラクト：

0x61b397ade3ed9c1511abff20a3a4701a3a52ecdc

このリポジトリのコードは、上記コントラクトを変更するものではありません。将来新規デプロイを行う場合は、別のコントラクトアドレスが発行されます。移行・配布基準も現時点では未確定です。

0628DAOにおける位置付け
0628DAOはトークン名ではなく、複数の専門知性と人間の最終責任を組み合わせるガバナンス構想です。EMAはその統治対象の一つであり、0628DAOそのものではありません。

本リポジトリに含まれるのは新EMAの基礎トークンとdApp接続方針です。0628BET本体、予測市場のロジック、フロントエンドおよびガバナンス執行機構は、別コントラクト・別工程として設計、検証、公開します。

設計方針
トークン本体は標準的で小さなERC-20実装に保つ

dApp固有の機能は別のプロトコルコントラクトへ分離する

dAppからは IERC20 / IERC20Permit として接続する

トークン移動にはOpenZeppelin SafeERC20 の利用を前提とする

TAX、Reflection、自動分配、DEXペア判定をトークン本体へ埋め込まない

後発Mint経路を設けない

リポジトリの内容
EMA_Draft.sol — 暫定ERC-20スマートコントラクト

EMA_dApp_Architecture_UTF8_BOM.txt — dApp対応方針とデプロイ前の検討事項

デプロイ前に確定・実施する事項
初期発行分の受取ウォレット

既存EMA保有者への移行・配布基準

制限機能を本体またはdApp側のどちらへ置くか

ERC20Votes 採用の要否

Arbitrum Sepoliaでのテスト

第三者によるセキュリティ監査

正式なデプロイアドレスの公開

重要事項
本コードは監査前・未デプロイです。

参照アドレスは既存EMAのものであり、本ドラフトのデプロイ先ではありません。

本リポジトリは、トークンの販売、投資勧誘、利益または価格上昇の保証を目的とするものではありません。

ウォレット接続や送金を行う前に、将来公式に告知されるネットワークとコントラクトアドレスを必ず照合してください。

仕様は検証・監査・法務確認の結果により変更される場合があります。

English summary
This repository contains a provisional Arbitrum One ERC-20 contract and a separated dApp architecture for a future EMADATA (EMA) relaunch, intended as the base token for the 0628BET Prediction Layer. The draft specifies a fixed supply of 777,000,000 EMA, 18 decimals, 0% transfer/buy/sell tax, no rewards or reflection, no later minting, self-burn only, and EIP-2612 Permit. It does not modify the existing EMA contract. The new draft has not been audited or deployed and is not an offer or promise of returns.

© 0628DAO. Development record for technical review.
