# Moonnet Saga ライセンス設計の検討案

更新日: 2026-08-29

この文書は、Moonnet Sagaを将来どの範囲までオープン化するかを検討するための設計メモです。**現時点のライセンスを変更するものではありません。**

現在の基本状態は引き続き All Rights Reserved です。

---

## 検討の背景

当初は、Moonnet Sagaの作品・設定を広く **CC BY-SA 4.0** で公開し、人間やAIが再利用・改変・再配布・派生創作できる共有創作宇宙にする案を検討していた。

ただし、CC BY-SA 4.0には **ShareAlike** 条件がある。

Creative Commons公式説明では、BY-SA 4.0でライセンスされた素材を remix / transform / build upon して Adapted Material を公開する場合、利用者自身の寄与にも同じライセンスまたは互換ライセンスを適用する必要がある。

この性質は「共有地を将来も共有地として拡張する」目的には強い一方、Moonnet Sagaの世界を使って独自の小説・漫画・ゲーム・映像等を作る第三者にとっては、作品のライセンス設計を制約する可能性がある。

Moonnet Sagaが優先したい価値が、

> 派生作品まで必ずオープンにすること

ではなく、

> 世界を誰でも創作の土台として使えること

であるなら、別の構成のほうが適している可能性がある。

---

## 案A — 作品・設定ともCC BY-SA 4.0

### 構成

- 原作小説: CC BY-SA 4.0
- 世界設定: CC BY-SA 4.0
- 年表・用語・人物設定: CC BY-SA 4.0
- JSON / YAML / Lorebook等: CC BY-SA 4.0

### 長所

- プロジェクト全体が一貫したオープンライセンスになる
- 改変版・派生版も共有可能な状態を維持しやすい
- Moonnet Saga由来の共有資産が継続的に増える可能性がある

### 短所

- Adapted Materialを公開する第三者にShareAlike義務が生じ得る
- 商業出版社、ゲーム会社、映像制作等が独自ライセンスで派生作品を展開しにくくなる可能性がある
- 「世界を使っただけ」の作品がどこまでAdapted Materialになるかは著作権法上の評価を含み、利用者に判断負担が生じる
- 原作本文自体も広範な複製・改変・商用利用の対象となる

### 向いている思想

**「この世界から生まれた派生物も、できる限り共有地へ戻してほしい」**

---

## 案B — 原作はAll Rights Reserved、世界設定はCC BY-SA 4.0

### 構成

- 原作小説: All Rights Reserved
- 世界設定・年表・用語等: CC BY-SA 4.0
- 機械可読データ: CC BY-SA 4.0
- 二次創作: 別途ガイドラインで歓迎

### 長所

- 原作本文の出版・販売上の自由度を保てる
- 世界設定を共有資産として育てられる
- 原作そのものを自由改変可能にする必要がない

### 短所

- 世界設定資料をAdapted Materialとして利用した派生作品には、なおShareAlikeが問題になり得る
- 「世界を使って自分の作品を作ってほしい」という目的に対して、BY-SAの義務が重い可能性がある

### 向いている思想

**「原作は守りたいが、世界設定の共有地はShareAlikeで育てたい」**

---

## 案C — 原作はAll Rights Reserved、世界設定はCC BY 4.0

現時点で有力な検討案。

### 構成

|層|候補となる扱い|
|---|---|
|原作小説本文|All Rights Reserved|
|商業出版作品|Saga本文には原則収録しない|
|公式World Bible|CC BY 4.0|
|年表・技術・用語・人物設定|CC BY 4.0|
|`world/` / `cosmology/`|対象を明示してCC BY 4.0|
|JSON / YAML / Lorebook等|CC BY 4.0|
|二次創作|別途Fan Works / Derivative Worksガイドラインで歓迎|
|Canon|作者が管理|
|Moonnet Saga名称・ロゴ等|CCとは別にブランド方針を管理|

### CC BY 4.0の特徴

Creative Commons公式説明では、CC BY 4.0は、クレジット等の条件を守れば、素材の共有・改変・商用利用を認める。

一方、BY-SAと異なり **ShareAlike条件はない**。

そのため、CC BY 4.0のWorld Bibleを利用して第三者が新しい作品を作る場合、その第三者の新規寄与について、Moonnet Saga側から同じCCライセンスを強制する設計にはならない。

### 長所

- 「世界を使って作品を作ってほしい」という目標と相性がよい
- 商業・非商業を問わず利用しやすい
- 派生作品の作者が、自分の作品をAll Rights Reserved、別のCCライセンス、商業契約等から選びやすい
- 原作小説の販売・出版戦略と世界設定のオープン化を切り分けられる
- KDP Select等の配信条件と、World Bible側のライセンスを分離しやすい

### 短所

- 第三者がWorld Bibleを改良・拡張しても、その改良版をオープンに戻す義務はない
- Moonnet Saga由来の派生設定が独占的に囲い込まれる可能性もある
- 原作小説にしか存在しない具体的な表現・台詞・ストーリー等までCC BYで利用できるわけではない

### 向いている思想

**「Stories are canon. The world is open.」**

または、

> 原作は公式作品として作者が保持する。  
> 世界設定は誰でも創作の土台にできる。  
> そこから生まれた作品の権利は、それぞれの作者が決められる。

---

## 重要: World BibleをCCにするだけでは、二次創作許諾の全てを処理できない

原作小説をAll Rights Reservedのまま残す場合、CC BY対象は **明示されたWorld Bible・設定資料の表現** に限られる。

たとえば、

- 原作小説の長い文章や台詞を転載する
- World Bibleにまだ記載されていないキャラクター描写を原作から直接利用する
- 原作のストーリーをそのまま改変する

といった利用までWorld BibleのCC BYだけで当然に許可されるとは限らない。

そのため、Moonnet Sagaとして「二次創作歓迎」を明確にするなら、CCライセンスとは別に **Fan Works / Derivative Works Policy** を用意する案がある。

このガイドラインでは、たとえば次を決める。

- 原作キャラクターを二次創作で利用してよいか
- 原作固有の出来事・設定を利用してよいか
- 商用二次創作を許可するか
- 成人向け、暴力的、政治的、宗教的表現等をどう扱うか
- 「公式」「公認」「Canon」と誤認させてはいけないこと
- クレジット方法
- ロゴ・商標の利用条件
- 原作本文の大量転載は禁止すること

つまり、

> **CC BY = 再利用できる公式設定資料のライセンス**  
> **Fan Works Policy = 原作IPを使った二次創作の許諾範囲**

と役割分担する設計。

---

## 現時点の有力候補

まだ決定ではないが、現在の議論からは次の構成が有力。

### Layer 1 — Stories

**All Rights Reserved**

- 公式小説
- 販売中の作品
- 将来商業出版する可能性がある原作

商業出版社から刊行された作品は、現在のプロジェクト方針どおりSaga本文へ原則収録しない。

### Layer 2 — Open Worldbuilding

**CC BY 4.0候補**

- World Bible
- 世界史・年表
- 技術
- 組織
- 用語
- キャラクターの再利用用プロフィール
- 世界間関係
- JSON / YAML
- Lorebook
- AI向け構造化データ

再利用してほしいキャラクターや設定については、原作から直接引用させるのではなく、**World Bible側へ再利用可能な形で改めて記述する**。

### Layer 3 — Fan / Derivative Works

**二次創作歓迎ガイドラインを別途設計**

第三者はMoonnet Sagaを使って新しい小説、漫画、ゲーム、映像、音楽、AI支援作品等を作れる。

派生作品は自動的に公式Canonにはならない。

派生作品そのもののライセンスをCC BY / BY-SAへ強制するかどうかは、現時点では **強制しない方向を有力候補** とする。

### Layer 4 — Canon / Brand

作者が管理。

- 公式Canonへの採用
- `Moonnet Saga`名称
- ロゴ
- 「公式」「公認」表示

は、コンテンツのオープンライセンスとは分離する。

---

## BY-SAを完全に捨てる必要はない

全てをCC BYに統一する必要もない。

たとえば、

- 基本World Bible: CC BY 4.0
- 共同編集する百科事典的データ: CC BY-SA 4.0
- 原作小説: All Rights Reserved

のように、用途ごとにライセンスを分けることも可能。

ただし複雑化すると利用者が理解しにくくなるため、実際に採用する場合は **ライセンス対象をファイル単位で機械的に判別できるmanifest** を用意する。

---

## 決定前に詰めること

- [ ] Moonnet Sagaの最優先目的は「共有地を拡張すること」か「創作の土台を広く提供すること」か
- [ ] 派生作品の作者にShareAlikeを要求したいか
- [ ] 商用二次創作を無条件で歓迎するか
- [ ] 原作キャラクターの利用をどこまで許可するか
- [ ] 原作ストーリーの翻案をどこまで許可するか
- [ ] World Bibleに何を再記述してCC対象にするか
- [ ] Canon / endorsement / trademarkのルール
- [ ] Fan Works PolicyをCC発効と同時に出すか
- [ ] `world/` / `cosmology/` の既存文書をそのままCC対象にできるか権利確認する

---

## 現時点での暫定評価

Moonnet Sagaの目的が、

> 人間やAIがこの世界を読み、そこから自由に新しい作品を生み出せること

にあるなら、**原作本文をAll Rights Reservedで保持し、再利用用に整備したWorld Bible・構造化データをCC BY 4.0で公開し、二次創作は別ガイドラインで明示的に歓迎する構成**が、CC BY-SA 4.0一括適用より適合する可能性が高い。

これはまだ採用決定ではない。

実際にライセンスを発効するときは、[`open-license-checklist.md`](open-license-checklist.md) に沿って対象ファイル、権利、第三者素材、ブランド、二次創作条件を改めて確認する。

---

## 参考: Creative Commons公式資料

- CC BY 4.0: https://creativecommons.org/licenses/by/4.0/
- CC BY-SA 4.0: https://creativecommons.org/licenses/by-sa/4.0/
- CC BY-SA 4.0 Legal Code: https://creativecommons.org/licenses/by-sa/4.0/legalcode
- Creative Commons FAQ: https://creativecommons.org/faq/

CC BY-SA 4.0では、Adapted Materialを共有する場合にShareAlike条件が適用される。一方CC BY 4.0にはShareAlike条件がない。どの利用が著作権法上Adapted Materialに当たるかは、適用法と具体的利用に依存する。
