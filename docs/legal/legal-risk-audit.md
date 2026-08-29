# Moonnet Saga 法的・権利リスク監査

調査日: 2026-08-29

> [!IMPORTANT]
> この文書は、公開情報・公式資料・現行リポジトリをもとにした実務上のリスク整理です。個別案件についての法律意見ではありません。契約書の解釈、権利帰属、侵害の成否など最終判断が必要な事項は、弁護士・弁理士等の専門家確認を前提とします。

## Executive summary

現時点の Moonnet-Saga は、`RIGHTS.md` で **All Rights Reserved** とし、CC BY-SA 4.0 は将来構想に留め、次の状態を別軸として管理している。

- Moonnet Saga に属するか
- Canon か
- GitHub で公開するか
- オープンライセンス対象か

この分離は妥当であり、**リポジトリ全体へ一括してCCライセンスを付けない現在の設計は維持すべき**。

現時点で見つかった優先事項は次のとおり。

|優先度|論点|要点|
|---|---|---|
|High / current check|過去の掲載・出版・配信契約|public GitHub自体が一定の利用許諾を伴うため、CC化前だけでなく現在の全文公開についても権利確認が必要|
|High if Select active|KDP Select / Kindle Unlimited|抜粋公開は一律禁止ではないが、現在公開している短編集収録3作は合計約34.7%で「少量サンプル」とは言いにくい。現行契約上の扱いは要確認|
|High before open licensing|CC対象の限定|作品・版・設定資料を明示列挙し、権利確認済みだけを対象にする|
|Medium|GitHub Termsの明示|public repoではGitHub機能上のFork等に加え、2026年のTermsではGitHub/関連会社のAI・ML訓練等に必要なライセンスも付与される|
|Medium before external PRs|Contribution権利処理|第三者の創作的PRを将来再ライセンスできるよう、受入条件またはCLA等を先に決める|
|Medium|現行READMEの将来構想表現|「Read it. Fork it. Build your own branch.」等が、現在すでに二次利用可能だと切り取られて誤解される余地がある|
|Low / Medium|名称・商標|完全一致の著名な同名は通常Web検索では確認できないが、J-PlatPatによる正式な類似検索は未完了|

**今すぐライセンスを変更する必要はない。**
次の一手は、`works-rights-matrix.md` の「要確認」を埋めることである。

---

## 1. 現在の公開状態

2026-08-29時点で、このリポジトリに作品本文として収録されているのは次の5作。

- マイニングファームにて
- アウトサイドフィールズ
- いいじいえいあい
- タカシ
- ワンダリングリング

リポジトリのGit treeを確認した範囲では、現在はMarkdownのみで、表紙画像・写真・音声・フォント等のバイナリ第三者素材は収録されていない。この点では現状の第三者素材リスクは比較的小さい。

ただし、本文内の引用、編集者等の創作的寄与、過去の掲載契約まではGit treeだけでは判定できない。

---

## 2. KDP Select / Kindle Unlimited と「一部公開」

### 結論

**「KDP Selectなら作品の一部も一切公開できない」という理解は正確ではない。**

Amazon自身の `Read Sample` はreflowable eBookについて通常10%を表示している。また、長年のKDPサポート案内では、外部サイトでのサンプル・抜粋について「約10%程度」が目安として案内されてきた事例が確認できる。

一方、**2026年現在の公開KDP Select契約本文には「外部公開は10%まで可」という数値のsafe harborは明記されていない**。現行契約は、Select期間中に `Digital Book (or a book that is substantially similar)` をデジタル形式で他所に販売・配布できない、という書き方になっている。

したがって、10%は実務上有力な目安ではあるが、現行契約本文だけから「10%以下なら必ず適法」と断定しない。

### 『ワンダリングリング 山田佳江SF短編集』について

Corpusにある2022年短編集版を文字数ベースで概算すると、8作品本文の合計は約46,204文字（段落間改行を含む単純計数）。

|作品|概算文字数|短編集本文に占める割合|
|---|---:|---:|
|アウトサイドフィールズ|5,954|約12.9%|
|いいじいえいあい|3,161|約6.8%|
|砂糖楓|1,459|約3.2%|
|タカシ（2022短編集版）|7,039|約15.2%|
|虚偽記憶の共犯者|5,603|約12.1%|
|おとなになれないきみたちとふたたび|3,273|約7.1%|
|昂奮ブロマイド|12,822|約27.8%|
|ワンダリングリング|6,893|約14.9%|

現在Sagaで2022短編集版そのものを全文公開している3作、

- アウトサイドフィールズ
- いいじいえいあい
- ワンダリングリング

の合計は**約34.7%**。

このため、仮に『ワンダリングリング 山田佳江SF短編集』が現在KDP Select登録中であれば、これら3作の全文公開を「通常の10%前後の宣伝用サンプル」として当然に扱えるとは言いにくい。

### 短編集特有の未確定点

現行KDP資料は、複数作品を含む本についてもKDP Selectのガイドラインを満たす必要があり、Select登録にはKindle eBookのprimary contentについて必要な独占的権利を保有することを求めている。

ただし公開契約文からは、**短編集に含まれる独立した短編1作の別公開が、常に「Digital Bookまたはsubstantially similar bookの配布」に当たるのか**を明確には読み取れない。

したがって、Selectが現在有効なら、KDPサポートへ次の形で確認するのが最も確実。

> 短編8作を収録したKDP Select登録中の短編集について、収録短編のうち数作を著者自身のWeb/GitHubで全文公開することはSelect exclusivityに抵触するか。短編集全体の約35%に相当するが、各短編は独立作品である。

### 『タカシ』について

Saga側の `works/takashi/text.md` はオルタニア7号提出稿ベースで、2022短編集版とは本文差がある。

この版差はリスクを下げる可能性があるが、KDP Select契約には `substantially similar` という文言があるため、**版が違えば自動的に対象外**とも断定しない。

### 評価

**High if KDP Select currently active / otherwise Low**

### 対応

- KDP Bookshelfで現在のSelect登録状態を確認
- 登録中ならKDPサポートに短編集＋独立短編のケースとして確認
- 回答をCorpus側の内部カルテに保存
- 状態確認が終わるまでは、短編集収録版へのCC BY-SA適用は保留
- Select非登録なら、この論点は原則として解消

公式資料:

- Amazon KDP Select: https://kdp.amazon.com/en_US/select
- How to enroll in KDP Select: https://kdp.amazon.com/en_US/help/topic/GD9PMU58BV24QFZ7
- KDP Terms and Conditions: https://kdp-eu.amazon.com/agreement
- Read Sample: https://kdp.amazon.com/en_US/help/topic/G200644250
- Guide to Kindle Content Quality (multi-work books): https://kdp.amazon.com/en_US/help/topic/G200952510

---

## 3. 過去の掲載・出版・電子配信契約

### なぜCC化前だけの問題ではないか

著作者本人が著作権を持っていても、著作権の譲渡、利用許諾、出版権の設定等があり得る。

日本の著作権法には、

- 第61条: 著作権の譲渡
- 第63条: 著作物の利用の許諾
- 第79条・第80条: 出版権

がある。

さらに現在のGitHub Termsでは、public repositoryにコンテンツを置くと、GitHubおよび他ユーザーへサービス提供上の一定のライセンスを付与する。そのため、過去の契約で独占的な公衆送信権等が設定されていた場合は、**CC BY-SAを付けていなくても現在のpublic全文公開に影響する可能性がある**。

### オルタニア掲載作

少なくとも次の作品には過去掲載歴がある。

- アウトサイドフィールズ — SF雑誌オルタニア Vol.18（2022）
- いいじいえいあい — SF雑誌オルタニア 増刊号 vol.9.999（2021）
- タカシ — SF雑誌オルタニア vol.7［後継種］（2018）
- 虚偽記憶の共犯者 — オルタニア バイキング増刊号9.5（2020）
- おとなになれないきみたちとふたたび — オルタニア vol.7.5（2019）
- 昂奮ブロマイド — オルタニア vol.6（2018）

『タカシ』を含むオルタニア号は複数の電子書店で販売された履歴が確認できる。

### 確認する資料

作品単位で次を探す。

- 投稿・寄稿時の募集要項
- メール、DM、契約書
- 紙・電子の出版権設定の有無
- 独占／非独占
- 公衆送信権、電子配信権、再配信権、二次利用
- 契約期間・終了条件
- 改稿版・再録版への適用範囲
- 編集者等による創作的な本文変更

契約資料が見つからない場合も「権利問題なし」と推測せず、`要確認` として残す。

### 評価

**High for currently published texts until basic history is confirmed / Needs contract review before CC activation**

公式資料:

- e-Gov 著作権法: https://laws.e-gov.go.jp/law/345AC0000000048
- KDP Intellectual Property Rights FAQ: https://kdp.amazon.com/en_US/help/topic/G200672400

公開書誌の確認例:

- BCCKS オルタニア vol.7: https://bccks.jp/bcck/157010/info
- BOOK☆WALKER オルタニア vol.7: https://bookwalker.jp/de0e074d1c-a6ac-4607-9f2c-279f2c1262e2/

---

## 4. GitHub public repository と現在の権利状態

### publicにすると何が起きるか

GitHubの2026年版Terms of Serviceでは、public repositoryについて概ね次の権利関係が生じる。

1. 他ユーザーはGitHub上で閲覧・Fork等を行える
2. GitHubはサービス提供・開発・改善に必要な範囲で保存・表示・解析・複製等を行える
3. 現行Termsでは、GitHubおよび関連会社のAI/MLモデル・技術の訓練、開発、改善も上記ライセンスの範囲に明示されている
4. repositoryに別のライセンスを置けば、その追加権利を利用者へ与えられる

### All Rights Reservedとの関係

したがって `All Rights Reserved` は、

> GitHub Terms、法令上の権利制限、その他別途の許諾により認められる範囲を除き、一般公衆へ追加の再利用ライセンスを付与していない

という意味で使うのが正確。

これは現在の `RIGHTS.md` の趣旨と大きく矛盾しない。

ただし、**GitHubへの契約上の利用許諾はすでに発生している**ため、過去の出版社等に強い独占権が残る作品では「All Rights Reservedだから安全」とはならない。

### 評価

**Medium as documentation / potentially High if an old contract is exclusive**

### 推奨追記

将来 `RIGHTS.md` を直す際は、次の趣旨を一文追加するとよい。

> Public availability on GitHub does not grant a general open-content license. Rights necessary for GitHub and its users to operate and use GitHub's service features are governed separately by GitHub's Terms of Service.

公式資料:

- GitHub Terms of Service: https://docs.github.com/en/site-policy/github-terms/github-terms-of-service
- GitHub Licensing a repository: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository

---

## 5. CC BY-SA 4.0

### Moonnet Sagaとの相性

CC BY-SA 4.0は次を認める。

- 複製・再配布
- 改変・翻案
- 商用利用
- あらゆる媒体・形式での利用

条件は主に、

- Attribution
- ShareAlike
- 追加的な法的・技術的制限を課さないこと

であり、「人間とAIが読み継ぎ、派生創作し、商用利用もできるfictional commons」という目標とは相性がよい。

### 不可逆性

CC BY-SA 4.0は取消不能。

作者が後で配布を停止することはできるが、既に適法にCCライセンスを受けた人は、その条件で利用を継続できる。

### CCが処理しないもの

CC BY-SA 4.0は万能な「IP全部入り」ライセンスではない。

- 商標権・特許権は許諾対象外
- 著作者人格権そのものはライセンスされない
  - ただし許諾された利用に必要な限定範囲で、権利者は可能な限り不行使等を行う仕組み
- 第三者のプライバシー、パブリシティ等は別問題
- 法律上の権利制限で許諾不要な利用にはCC条件自体が適用されない

### 推奨方式

リポジトリ全体へ一括適用せず、対象を明示する。

例:

```text
License status:
- works/takashi/text.md: CC BY-SA 4.0 (effective YYYY-MM-DD)
- world/works/takashi.md: CC BY-SA 4.0 (effective YYYY-MM-DD)
- README / governance docs: separate status
- third-party quotations/materials: excluded
```

最低限、次を示す。

- 対象作品
- 対象版
- 対象ファイル
- 発効日
- 除外物
- 推奨クレジット
- 商標は対象外
- Saga status / Canon statusとは別であること

### 評価

**Medium now / High at activation**

公式資料:

- CC BY-SA 4.0: https://creativecommons.org/licenses/by-sa/4.0/
- Legal Code: https://creativecommons.org/licenses/by-sa/4.0/legalcode.en
- Creative Commons FAQ: https://creativecommons.org/faq/
- CC License Your Work: https://creativecommons.org/cc-license-your-work/

---

## 6. 著作者人格権

日本の著作権法上、著作者人格権には公表権、氏名表示権、同一性保持権等があり、一身専属で譲渡できない。

CC BY-SA 4.0は人格権そのものを移転するわけではなく、ライセンス利用に必要な限定範囲で可能な限り不行使等をする構造。

Moonnet Sagaでは、原作者と異なる価値観、成人向け、政治的、宗教的表現等を含むbranchも許容する将来像をすでにREADMEに書いている。

これは十分に意識的な設計だが、実際にCC化する前に作者が、

- 大幅な改変
- キャラクター性格の変更
- 原作と逆の政治的・宗教的主張
- 成人向け化
- 商用広告への利用

等もCC BY-SAの範囲で起こり得ることを理解した上で採用する必要がある。

**「気に入らない改変だけ後から禁止する」ライセンスにはならない。**

### 評価

**Medium / author decision before activation**

法令:

- e-Gov 著作権法 第18〜20条、第59条
- https://laws.e-gov.go.jp/law/345AC0000000048

---

## 7. AI利用

### 日本法とCCは別レイヤー

文化庁は、AI学習・生成における著作物利用をすべて「著作権者のライセンスが必要」とは整理していない。

著作権法第30条の4等の権利制限が適用される利用なら、CC BY-SAを根拠にしなくても利用できる場合がある。

Creative Commonsのリーガルコードも、法令上の例外・権利制限が適用される場合にはCC条件に従う必要はないと明記する。

したがって、将来の説明では、

- 「CC BY-SAだからAI学習できる」
- 「AIに読み込ませたら必ずShareAlike」
- 「AI生成物は必ず著作物」

のような単純化は避ける。

### AI生成物の著作物性

文化庁は、AIを人の創作の「道具」として利用したといえるかについて、

- 創作意図
- 人の創作的寄与

等を総合的に判断する必要があるとしている。

### GitHub自身のAI利用

別論点として、現在のGitHub Termsでは、GitHubおよび関連会社がサービスの開発・改善のためAI/MLモデル等を訓練する権利が明記されている。

これは「CC BY-SAを発効したから生じる」ものではなく、**public GitHubへ投稿する契約レイヤーで既に存在する**。

Moonnet SagaはAI利用を歓迎する方向なので理念上は衝突しにくいが、権利管理上は把握しておく。

### 評価

**Low now / Medium for future user guidance**

公式資料:

- 文化庁「AIと著作権について」: https://www.bunka.go.jp/seisaku/chosakuken/aiandcopyright.html
- 文化審議会「AIと著作権に関する考え方について」（令和6年3月15日）
- 文化庁「AIと著作権に関するチェックリスト＆ガイダンス」（令和6年7月31日）
- 文化庁 著作権分科会報告書等: https://www.bunka.go.jp/seisaku/bunkashingikai/chosakuken/hokoku.html

2026年時点でもAI・著作権政策は更新が続いているため、実際のオープンライセンス発効時に最新情報を再確認する。

---

## 8. 第三者Contribution

現在は `CONTRIBUTING.md` やCLA等がない。

GitHub Termsでは、repositoryにライセンス表示がある場合、原則としてContributionもそのライセンス条件で提供される。一方、現在のMoonnet-Sagaには一般公衆向けのオープンライセンスがない。

この状態で第三者から創作的な、

- 新規小説
- キャラクター設定
- 世界設定
- 長文の改稿
- イラスト等

を受け取りマージすると、将来プロジェクト全体をCC BY-SAへ移行したくても、そのContributionを山田佳江単独の判断で再ライセンスできない可能性がある。

### 現時点の推奨

外部Contributionを積極募集する前に、次のどれかを決める。

1. **Inbound = outbound**
   - CC化後、Contributorも同じCC BY-SA 4.0で投稿
2. **Contributor agreement**
   - プロジェクトにCC BY-SA 4.0等で公開・再ライセンスする権利を明示的に許諾
3. **創作的Contributionは受け付けず、誤字・リンク修正等に限定**

DCO（Developer Certificate of Origin）は「投稿権限があること」の確認には使えるが、独自の再ライセンス権を自動的に与えるものではないため、目的に応じてCLA等と区別する。

### 評価

**Medium now / High before creative external contributions**

---

## 9. Canon / Saga / Public / License の4軸

現在の設計では、少なくとも次の4状態を分離できている。

|軸|意味|
|---|---|
|Saga status|Moonnet Sagaに属するか (`confirmed / possible / excluded`)|
|Canon status|公式設定・公式作品として採用しているか|
|Public status|本文や設定がpublic repositoryに置かれているか|
|License status|CC BY-SA等の一般再利用ライセンス対象か|

これは非常に良い。

たとえば、

- `possible` だが本文public
- `confirmed` だが本文未公開
- `confirmed` かつpublicだがAll Rights Reserved
- `confirmed` / public / CC BY-SA

を別々に表現できる。

**この4軸を今後も統合しない。**

---

## 10. READMEの「Open Story IP」表現

READMEは繰り返し「現在はオープンライセンス移行前」と明記しているため、全体としては安全側。

ただし、

> Read it. Fork it. Build your own branch.

というコピーは、単独で検索結果やSNSに抜かれた場合、現時点でも二次創作を一般許諾済みと誤認される可能性がある。

緊急修正ではないが、CC発効前は、

> Future vision: Read it. Fork it. Build your own branch.

等にするとより明確。

### 評価

**Low / Medium documentation clarity**

---

## 11. 商標・ブランド

### Web上の簡易調査

通常のWeb検索では、2026-08-29時点で、

- `Moonnet Saga`
- `ムーンネットサーガ`
- `Open Story IP`

について、同一の著名な作品シリーズ・サービスの完全一致は確認できなかった。

ただし `MoonNet` / `MOONNET` 単独では、

- AI/機械学習プロジェクト名
- 海外企業名
- 商品名
- 過去のカード商品等

複数の使用例がある。

したがって、`Moonnet` 単独の独占可能性・登録可能性はこの調査から判断できない。

### J-PlatPat

特許庁はJ-PlatPatを使った先行商標調査を案内しているが、この調査環境からJ-PlatPatの動的な検索結果を証拠として安定取得できなかった。

正式な商標クリアランスは未完了。

最低限、次をJ-PlatPatの「商標（検索用）」および称呼検索で確認する。

- Moonnet Saga
- MOONNET SAGA
- ムーンネットサーガ
- Moonnet
- MOONNET
- ムーンネット
- Open Story IP

実際に商標出願を検討する段階では、使用予定の商品・役務区分も含め弁理士確認が望ましい。

### 評価

**Low now / Medium before major branding investment**

公式:

- 特許庁「商標を検索してみましょう」: https://www.jpo.go.jp/support/startup/shohyo_search.html
- J-PlatPat: https://www.j-platpat.inpit.go.jp/

---

## 12. 第三者素材・引用

現在のGit treeにはMarkdown以外の画像・音声・フォント等は見当たらない。

将来CC化する作品・資料については、作品単位で次を確認する。

- 歌詞・詩・小説等からの引用
- 他者の写真、イラスト、地図
- 表紙・装丁
- 編集者・共同作者による創作的文章
- 実在人物の写真・肖像・プライバシー情報
- 他者が権利を持つ翻訳
- 外部資料から転記した設定説明

第三者素材を含む場合は、その部分をCC対象から明示的に除外することができる。

Creative Commons自身も、ライセンサーが権利を持たない素材は明確にマークして除外することを推奨している。

### 評価

**Medium before CC activation**

---

## 13. 現在のリポジトリに対する提案

### すぐ確認する（人間の管理画面・手元資料が必要）

1. 『ワンダリングリング 山田佳江SF短編集』の現在のKDP Select状態
2. オルタニア等の寄稿・掲載条件の所在
3. 公開中5作について、独占的な電子配信・出版権が残っていないか

### GitHubだけで後から改善できる

1. `RIGHTS.md` にGitHub Termsとの関係を一文追記
2. `Read it. Fork it. Build your own branch.` を将来構想と明示
3. 外部Contributionを始める前に `CONTRIBUTING.md` を作成
4. `WORKS.md` に将来 `License status` 列を追加
5. CC発効時には対象作品・版・ファイルを列挙したmanifestを作る

### 今はしない

- repository rootへCC BY-SAの `LICENSE` を置く
- repository全体を一括CC化する
- `possible` だから自動的にCC対象にする
- 契約未確認作品をオープン化する

---

## 14. Open-license release gate

CC BY-SA 4.0を実際に発効する前に、次をすべて確認する。

- [ ] 対象作品について著作権帰属を確認
- [ ] 過去の出版権・独占利用許諾・電子配信権を確認
- [ ] KDP Select等の独占条件と衝突しない
- [ ] 対象版を特定
- [ ] 対象ファイルを特定
- [ ] 第三者素材を除外または個別表示
- [ ] 作者が取消不能・商用利用・翻案・ShareAlikeを理解して選択
- [ ] Canon / Saga / Public / License statusを別管理
- [ ] 商標・ブランドはCC対象外と明示
- [ ] attribution推奨形式を決定
- [ ] 外部Contribution方針を決定
- [ ] README / RIGHTS / WORKS / 各作品READMEの表示を一致
- [ ] 発効日を記録
- [ ] 発効直前に法制度・GitHub Terms・販売契約を再確認

詳細な作業用チェックリストは [`open-license-checklist.md`](open-license-checklist.md) を参照。

---

## Sources

一次資料・公式資料を優先した。

### 日本法・AI

- e-Gov 著作権法: https://laws.e-gov.go.jp/law/345AC0000000048
- 文化庁「AIと著作権について」: https://www.bunka.go.jp/seisaku/chosakuken/aiandcopyright.html
- 文化庁 著作権分科会 報告・答申等: https://www.bunka.go.jp/seisaku/bunkashingikai/chosakuken/hokoku.html

### Creative Commons

- CC BY-SA 4.0: https://creativecommons.org/licenses/by-sa/4.0/
- Legal Code: https://creativecommons.org/licenses/by-sa/4.0/legalcode.en
- FAQ: https://creativecommons.org/faq/
- License Your Work: https://creativecommons.org/cc-license-your-work/

### GitHub

- Terms of Service: https://docs.github.com/en/site-policy/github-terms/github-terms-of-service
- Licensing a repository: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository

### Amazon KDP

- KDP Select: https://kdp.amazon.com/en_US/select
- How to enroll in KDP Select: https://kdp.amazon.com/en_US/help/topic/GD9PMU58BV24QFZ7
- KDP Terms and Conditions: https://kdp-eu.amazon.com/agreement
- Read Sample: https://kdp.amazon.com/en_US/help/topic/G200644250
- Kindle Content Quality: https://kdp.amazon.com/en_US/help/topic/G200952510
- Intellectual Property Rights FAQ: https://kdp.amazon.com/en_US/help/topic/G200672400

### 商標

- 特許庁「商標を検索してみましょう」: https://www.jpo.go.jp/support/startup/shohyo_search.html
- J-PlatPat: https://www.j-platpat.inpit.go.jp/

---

## 調査上の限界

- 非公開の出版契約書、メール、DMは確認していない
- KDP管理画面の現在のSelect登録状態は確認していない
- KDPの「外部サンプル約10%」について、現行公開契約本文には数値規定が見つからないため、確実なsafe harborとして扱っていない
- J-PlatPatの正式な類似商標検索結果は取得できていない
- 各小説本文を既存著作物と逐語的・網羅的に照合する引用監査はしていない
- 海外各国の著作権法を国別に精査していない

このため、本調査の次の一手は**ライセンス変更ではなく、作品ごとの権利事実を埋めること**である。
