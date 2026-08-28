# Moonnet Saga 作品別権利確認マトリクス

更新日: 2026-08-29

この表は、Moonnet Saga作品を将来オープンライセンス化する前に、**作品ごと・版ごとに権利確認を進めるための作業台帳**。

`要確認` は問題があるという意味ではなく、現時点で根拠資料が未登録という意味。

## Status

- `OK candidate` — 現時点で大きな外部権利要因が見えていない。ただしCC発効前の最終確認は必要
- `Check publishing rights` — 過去掲載・販売等があり、契約・利用許諾等を確認する
- `Check KDP Select` — KDP Selectが現在有効なら追加確認が必要
- `Not current candidate` — Saga未判定・possible等の理由で、今すぐCC対象にする必要がない
- `Professional review if unclear` — 契約書の文言等で判断が難しい場合

## 作品一覧

|作品|Saga status|Saga本文|既知の初出・状態|主な確認事項|CC化前の状態|
|---|---|---|---|---|---|
|アンフォールドザワールド|`possible`|未収録|SF雑誌「ガンズ」|掲載・出版条件、版、現在の権利帰属|Check publishing rights / Not current candidate|
|暁の夜|`confirmed`|未収録|未完稿|共同制作・第三者素材の有無、どの版を公開するか|OK candidate after provenance check|
|ボタニカルアリス|`confirmed`|未収録|公開・刊行歴確認中|過去の単独電子版等の権利・販売履歴を確定|Check publishing rights|
|十＋十|`possible`|未収録|執筆中|完成後の版、共同制作・AI生成部分があればその扱い|Not current candidate|
|マイニングファームにて|`possible`|公開中|初出確認中|初出媒体・掲載条件を確定。公開版の出典版を固定|Check publishing rights / Not current CC candidate|
|アウトサイドフィールズ|`possible`|公開中|オルタニア Vol.18（2022）、2022短編集収録|オルタニア掲載条件、短編集KDP Select状態、公開している2022版の扱い|Check publishing rights + Check KDP Select|
|いいじいえいあい|`possible`|公開中|オルタニア 増刊号 vol.9.999（2021）、2022短編集収録|オルタニア掲載条件、短編集KDP Select状態、公開している2022版の扱い|Check publishing rights + Check KDP Select|
|砂糖楓|—|未収録|てきすぽどーじん6号（2013）、2022短編集収録|Saga判定前。初出条件、短編集の扱い|Not current candidate|
|タカシ|`confirmed`|公開中|オルタニア vol.7［後継種］（2018）、2022短編集収録|Saga公開版は提出稿ベース。オルタニア掲載条件、2022版との差、KDP Selectの`substantially similar`扱い|Check publishing rights; KDP clarification if Select active|
|虚偽記憶の共犯者|—|未収録|オルタニア バイキング増刊号9.5（2020）、2022短編集収録|Saga判定前。掲載条件、短編集の扱い|Not current candidate|
|おとなになれないきみたちとふたたび|—|未収録|オルタニア vol.7.5（2019）、2022短編集収録|Saga判定前。掲載条件、短編集の扱い|Not current candidate|
|昂奮ブロマイド|—|未収録|オルタニア vol.6（2018）、2022短編集収録|Saga判定前。掲載条件、短編集の扱い|Not current candidate|
|ワンダリングリング|`possible`|公開中|2022短編集書き下ろし|短編集KDP Select状態。GitHub公開版は短編集版そのもの|Check KDP Select / Not current CC candidate|

## 現在公開中5作の優先確認

### 1. タカシ

現在Saga側で公開しているのは、オルタニア7号提出稿ベース。

確認するもの:

- オルタニア7号への寄稿・掲載条件
- 電子販売に関する契約・許諾
- 提出稿を作者が独自公開できること
- 2022短編集版との権利・版の関係
- KDP Selectが有効な場合、旧稿が `substantially similar` と評価される可能性

CC化する場合は、必ず「どの版」を対象にするか明示する。

### 2. アウトサイドフィールズ

現在Saga側は2022短編集版を公開。

確認するもの:

- オルタニア Vol.18掲載条件
- 再録時の権利
- 2022短編集の現在のKDP Select状態
- KDP Select中の場合、短編全文公開が許容されるか

2022短編集本文全体に対する概算文字数比は約12.9%。

### 3. いいじいえいあい

現在Saga側は2022短編集版を公開。

確認するもの:

- オルタニア vol.9.999掲載条件
- 再録時の権利
- 2022短編集の現在のKDP Select状態
- KDP Select中の場合、短編全文公開が許容されるか

2022短編集本文全体に対する概算文字数比は約6.8%。

### 4. ワンダリングリング

2022短編集書き下ろしで、Saga側は同版を公開。

掲載誌由来の外部契約リスクは他の3作より少ない可能性がある一方、KDP Selectが有効なら短編集との同一性が最も明確。

2022短編集本文全体に対する概算文字数比は約14.9%。

### 5. マイニングファームにて

初出詳細がまだ不明。

最初に、

- 初出媒体
- 提出先
- 掲載・販売の有無
- その際の条件

を確定する。

## Corpusに追加しておくとよい内部情報

各作品カルテへ、可能なら次を追記する。

```text
## Rights / publication history

- copyright owner:
- first-publication agreement:
- exclusivity:
- publication right:
- electronic distribution:
- contract term:
- rights reverted / expired:
- KDP title:
- KDP Select status:
- third-party creative material:
- evidence:
- last checked:
```

ここには公開すると不要に個人情報・契約情報が出る資料もあるため、詳細はprivate Corpusに持ち、Moonnet-Saga側には結果だけを反映する。

## CC化判定の最低条件

作品ごとに次が全部 `yes` になったときだけ、CC候補へ進める。

|確認|yes/no|
|---|---|
|山田佳江が対象版の著作権を必要範囲で保有している| |
|第三者との独占契約に抵触しない| |
|出版権等に抵触しない| |
|KDP Select等の独占条件に抵触しない| |
|第三者著作物を除外または適法に処理した| |
|対象版を特定した| |
|対象ファイルを特定した| |
|作者がCC BY-SA 4.0の取消不能性を理解した| |
|商標・Canon・endorsementとライセンスを分離した| |

全項目確認後、[`open-license-checklist.md`](open-license-checklist.md)へ進む。
