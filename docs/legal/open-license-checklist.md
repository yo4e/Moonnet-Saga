# Moonnet Saga オープンライセンス移行チェックリスト

更新日: 2026-08-29

Moonnet Sagaの作品・設定をCC BY-SA 4.0等で実際にオープン化するときの作業用チェックリスト。

> [!WARNING]
> **このチェックリストが終わる前に、repository rootへCCライセンスを一括適用しない。**
> Creative Commonsライセンスは、一度有効に付与すると原則として取消不能。

## Phase 0 — 今はまだ発効しない

- [ ] `RIGHTS.md` に「proposal / future direction」と明記されている
- [ ] rootに誤解を招くCC `LICENSE` が置かれていない
- [ ] 各作品が現時点では All Rights Reserved であることを確認
- [ ] Saga statusとlicense statusを別管理している

## Phase 1 — 対象を決める

### 作品

- [ ] オープン化する作品名を列挙
- [ ] 作品ごとにSaga statusを確認
- [ ] Canonかどうかを別途確認
- [ ] `possible`だから自動的に対象にしない

### 版

- [ ] 対象版を特定
- [ ] 初出版／提出稿／単行本版／改稿版を混同していない
- [ ] 複数版がある場合、どの版だけがCC対象か明記
- [ ] `タカシ` 等は版差を確認

### ファイル

- [ ] 対象ファイルをパス単位で列挙
- [ ] `works/<slug>/text.md` のどれを対象にするか確認
- [ ] `world/` や `cosmology/` を含めるか別途決定
- [ ] READMEやガバナンス文書まで同じライセンスにする必要があるか検討

## Phase 2 — 著作権・契約

各作品について:

- [ ] 著作者を確認
- [ ] 著作権の譲渡有無を確認
- [ ] 共同著作物ではないこと、または共同著作者の同意を確認
- [ ] 出版権設定の有無を確認
- [ ] 独占利用許諾の有無を確認
- [ ] 公衆送信・電子配信の契約を確認
- [ ] 契約期間を確認
- [ ] 権利返還・契約終了がある場合、証拠を保存
- [ ] オルタニア等の寄稿条件を確認
- [ ] KDP / Kindle関連の条件を確認

判断が難しい契約文言:

- [ ] 必要なら弁護士等へ相談

## Phase 3 — KDP Select / 配信サービス

短編集・電子書籍がKDP Select等に参加している場合:

- [ ] 現在の登録状態をKDP Bookshelfで確認
- [ ] 90日間のSelect期間を確認
- [ ] 自動更新状態を確認
- [ ] GitHubで公開している内容が独占条件に抵触しないか確認
- [ ] 短編集の場合、収録短編の独立公開についてKDPサポートへ必要に応じて確認
- [ ] KDPサポート回答をprivate Corpusに保存
- [ ] Select中にCC化しないことを確認

『ワンダリングリング 山田佳江SF短編集』では、2022版ベースでSaga公開中3作が短編集本文の概算約34.7%に相当するため、Selectが有効なら個別確認を優先。

## Phase 4 — 第三者素材

各対象ファイルについて:

- [ ] 他者の小説・詩・歌詞等の引用を確認
- [ ] 写真を確認
- [ ] イラストを確認
- [ ] 表紙・装丁を確認
- [ ] フォントデータを確認
- [ ] 地図・図表を確認
- [ ] 翻訳を確認
- [ ] 編集者・共同制作者の創作的寄与を確認
- [ ] 実在人物のプライバシー・肖像等を確認

第三者素材がある場合:

- [ ] CC対象から明示的に除外
- [ ] その素材固有の権利表示を記載
- [ ] 除外部分が読者に識別できるようにする

## Phase 5 — CC BY-SA 4.0の意思確認

作者が次を理解していることを確認。

- [ ] 商用利用を許可する
- [ ] 複製・再配布を許可する
- [ ] 翻案・改変を許可する
- [ ] 翻訳を許可する
- [ ] ゲーム化・漫画化・映像化等を許可する
- [ ] AI支援創作を想定する
- [ ] 派生作品のShareAlikeを要求する
- [ ] 条件に従う利用者へのライセンスは取消不能
- [ ] 気に入らない派生作品だけ後から禁止する仕組みではない
- [ ] CCは商標権をライセンスしない
- [ ] CCは第三者のプライバシー等を解決しない
- [ ] 法律上許諾不要なAI学習等までCC条件で拘束できるとは限らない

## Phase 6 — ブランド・Canon

- [ ] `Moonnet Saga` / `ムーンネットサーガ` の商標方針を決定
- [ ] 商標・ロゴはCC対象外とするか決定
- [ ] 「公式」「Canon」を名乗れる条件を決定
- [ ] CC利用者が公式認定を示唆できないことを明記
- [ ] `No endorsement` の説明を維持
- [ ] 第三者branchと公式Canonを明確に分離

## Phase 7 — Attribution

推奨クレジットを決める。

例:

```text
Based on "Moonnet Saga" by Yoshie Yamada / 山田佳江.
Licensed under CC BY-SA 4.0.
Source: <canonical URL>
Changes: <summary>
```

- [ ] 日本語表記を決定
- [ ] 英語表記を決定
- [ ] canonical URLを決定
- [ ] 改変表示の例を用意
- [ ] attributionがendorsementを意味しないことを明記

## Phase 8 — Contribution

第三者からPRを受けるなら発効前に決める。

- [ ] 誤字・リンク修正等の非創作的Contribution
- [ ] 世界設定
- [ ] 小説
- [ ] イラスト
- [ ] 翻訳
- [ ] データセット

権利条件:

- [ ] Contributorが必要な権利を持つことを表明
- [ ] inbound licenseを明記
- [ ] 必要ならCLAを採用
- [ ] Canon採用と権利許諾を別にする
- [ ] Contributor credit方針を決定
- [ ] 第三者素材の持込み禁止・申告ルールを決定

## Phase 9 — ライセンスmanifestを作る

例:

```yaml
effective_date: YYYY-MM-DD
license: CC-BY-SA-4.0

covered:
  - works/takashi/text.md
  - world/works/takashi.md

excluded:
  - trademark: "Moonnet Saga"
  - third_party_material: []
```

形式はMarkdownでもYAMLでもよいが、**対象範囲が機械的に判別できる状態**を推奨。

- [ ] covered files一覧
- [ ] excluded files一覧
- [ ] third-party exceptions
- [ ] 発効日
- [ ] license URL
- [ ] attribution
- [ ] Canon statusとは別だと明記

## Phase 10 — 文書整合

同じ日に次を確認。

- [ ] `README.md`
- [ ] `RIGHTS.md`
- [ ] `WORKS.md`
- [ ] 各 `works/<slug>/README.md`
- [ ] license manifest
- [ ] `CONTRIBUTING.md`
- [ ] repository About / description

矛盾がないこと。

## Phase 11 — Release

- [ ] 専用PRを作る
- [ ] PRに対象作品と対象版を列挙
- [ ] 権利確認の根拠をprivate Corpus側に記録
- [ ] PR差分を人間が確認
- [ ] 発効日を記録
- [ ] merge後のpublic表示を確認
- [ ] GitHubがライセンスを意図通り認識するか確認

## Phase 12 — 発効後

- [ ] 発効したCCライセンスを「撤回できる」と書かない
- [ ] 新しい版を追加するとき、ライセンス対象か都度判断
- [ ] 新しい作品を追加しただけで自動CC化しない
- [ ] 第三者素材追加時に除外表示を更新
- [ ] GitHub Terms / CC / 日本法 / 配信契約の変更を定期確認
- [ ] Canon変更とlicense変更を混同しない

---

関連:

- [`legal-risk-audit.md`](legal-risk-audit.md)
- [`works-rights-matrix.md`](works-rights-matrix.md)
