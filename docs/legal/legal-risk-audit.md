# Moonnet Saga 法的・権利リスク監査

調査日: 2026-08-29

> [!IMPORTANT]
> この文書は、公開情報・公式資料・現行リポジトリをもとにした実務上のリスク整理です。個別案件についての法律意見ではありません。契約書の解釈、権利帰属、侵害の成否など最終判断が必要な事項は、弁護士・弁理士等の専門家確認を前提とします。

## 結論

現時点の Moonnet-Saga は、`RIGHTS.md` で **All Rights Reserved** とし、CC BY-SA 4.0 は将来構想に留め、Saga所属・Canon・公開・オープンライセンス対象を別軸としている。この基本設計は安全側であり、**今すぐCC BY-SA 4.0へ移行しない限り、構造上の重大な問題は見つからなかった**。

ただし、オープン化以前に確認すべき重要事項がある。優先順位は次のとおり。

1. **High / immediate check — KDP Select / Kindle Unlimited の現在の登録状態**
2. **High — 過去の掲載・出版・電子配信について、契約・出版権・独占許諾の有無を作品単位で確認**
3. **High before open licensing — CC対象を作品・版・資料単位で明示し、権利確認済みのものだけにライセンスを付ける**
4. **Medium — public GitHub と All Rights Reserved の関係を文言上もう少し正確にする**
5. **Medium — 将来外部Contributionを受ける前に inbound license / CONTRIBUTING 方針を決める**
6. **Medium — `Read it. Fork it. Build your own branch.` 等、将来構想と現在の許諾を誤認し得る表現を整理する**
7. **Low/Medium — Moonnet Saga / ムーンネットサーガ等の商標スクリーニングを正式に行う**

## 1. KDP Select / Kindle Unlimited — 最優先確認

### リスク

『ワンダリングリング 山田佳江SF短編集』は現在もKindleで販売されていることを公開情報から確認できる。また、2023年のセルフパブ読書記録には同書についてKindle Unlimited対象であった可能性を示す記述がある。ただし、**2026-08-29現在のKDP Select登録状態は公開情報だけでは確認できなかった**。

Amazon KDP公式資料では、KDP Selectに登録した電子書籍はKindle Unlimitedに自動的に追加され、90日間の登録期間中、Kindle本のデジタル版は原則としてKindle Store独占とする必要がある。

Moonnet-Sagaでは現在、『ワンダリングリング』2022年版を出典とする次の全文を公開している。

- アウトサイドフィールズ
- いいじいえいあい
- ワンダリングリング

また『タカシ』も同短編集に収録されているが、Saga側の公開本文はオルタニア7号提出稿ベースであり、2022年短編集版とは本文差がある。

### 評価

**High / current status dependent**

KDP Selectが現在有効なら、同書の主要コンテンツをGitHubで全文公開することが独占要件と衝突する可能性がある。個々の短編を別媒体に公開した場合にどこまで「同じ電子書籍の主要コンテンツ」の独占条件に触れるかは、KDP契約・作品構成・版差を踏まえた確認が必要。

### 対応

- KDP Bookshelfで『ワンダリングリング 山田佳江SF短編集』の「KDP セレクトを管理」を開き、現在の登録期間を確認する。
- Select登録中なら、GitHub全文公開との整合をKDP規約に照らして確認する。
- 必要なら、Select更新停止／公開本文の一時撤去／別版扱いの検討を行う。
- **この確認が終わるまで、同短編集収録作をCC BY-SA化しない。**

公式資料:

- Amazon KDP「セルフ出版と KDP セレクト」: https://kdp.amazon.co.jp/ja_JP/select
- Amazon KDP「KDP セレクトへの登録方法」: https://kdp.amazon.co.jp/ja_JP/help/topic/GD9PMU58BV24QFZ7
- Amazon KDP「Kindle Unlimited」: https://kdp.amazon.co.jp/ja_JP/help/topic/G201537300

## 2. オルタニア等の過去掲載・出版契約

### 確認できたこと

少なくとも『タカシ』は『SF雑誌オルタニア vol.7［後継種］』に掲載され、BCCKS、BOOK☆WALKER、Apple Books、楽天Kobo等で販売された履歴が確認できる。オルタニア作品は複数著者による雑誌・電子書籍として流通している。

著作者本人が著作権を持っている場合でも、日本の著作権法上、著作権は全部または一部を譲渡でき、利用許諾も可能であり、さらに出版権を設定すると出版権者が設定範囲の権利を専有し得る。したがって「自分が書いた作品」という事実だけでは、現在CCライセンスを付与できる範囲を確定できない。

### 評価

**High before open licensing / Needs contract review**

現在の公開そのものが問題であると示す資料は見つかっていない。しかし、CC BY-SA 4.0は広範な複製・改変・商用利用を取消不能で許諾するため、掲載時の条件確認なしに付与すべきではない。

### 対応

各作品について次を探す。

- 投稿時・掲載時の募集要項
- メール、DM、契約書、利用許諾
- 紙・電子の出版権設定の有無
- 独占／非独占の別
- 電子配信権、再配信権、二次利用権
- 契約期間・終了条件
- 編集者等による本文への創作的修正の扱い

契約書がない場合も「契約がない」と推測せず、当時の募集要項ややり取りをCorpus側の内部カルテに保存する。

法令:

- e-Gov 著作権法: https://laws.e-gov.go.jp/law/345AC0000000048
  - 第61条 著作権の譲渡
  - 第63条 著作物の利用の許諾
  - 第79条・第80条 出版権

公開確認例:

- BCCKS オルタニア vol.7: https://bccks.jp/bcck/157010/info
- BOOK☆WALKER: https://bookwalker.jp/de0e074d1c-a6ac-4607-9f2c-279f2c1262e2/

## 3. CC BY-SA 4.0 の採用

### 現行方針の良い点

`RIGHTS.md` は次を明確に分離している。

- Moonnet Sagaに属するか
- Canonか
- GitHubで公開するか
- CC BY-SA 4.0対象か

この分離は維持すべき。

### CC BY-SA 4.0で重要な点

Creative Commonsの公式リーガルコード上、CC BY-SA 4.0は全世界・無償・非独占かつ**取消不能**の許諾で、複製・共有・翻案物の作成と共有を認める。

一方で、次はCCの許諾対象外または別扱い。

- 著作者人格権そのものはライセンスされない。ただし許諾された利用に必要な限定範囲で、可能な限り不行使等が規定される。
- 商標権・特許権はライセンスされない。
- プライバシー、パブリシティ等の人格権は別問題。
- 法律上の権利制限により許諾不要な利用には、そもそもCC条件は適用されない。
- 配布を後から停止しても、既に有効に与えたCCライセンス自体は終了しない。

### 評価

**Medium now / High at activation**

CC BY-SA 4.0自体は「人間・AIが再利用し、商用派生作品も作れる共有創作宇宙」というMoonnet Sagaの目標と整合しやすい。ただし、一括でリポジトリ全体に適用するより、**権利確認済み作品・設定を明示的に列挙して段階的に適用する**方が安全。

### 推奨方式

将来の移行時は少なくとも次を明示する。

- ライセンス開始日
- 対象ファイル／対象作品／対象版
- 対象外ファイル
- 第三者素材の除外
- 推奨クレジット表記
- Canon statusとは無関係であること
- 商標・ブランドの扱い

公式資料:

- CC BY-SA 4.0 Legal Code 日本語: https://creativecommons.org/licenses/by-sa/4.0/legalcode.ja
- CC BY-SA 4.0 Legal Code 英語: https://creativecommons.org/licenses/by-sa/4.0/legalcode.en

## 4. GitHub public repository と All Rights Reserved

GitHubの公式Termsでは、public repositoryにすると、他のGitHubユーザーに対し、GitHubの機能を通じた閲覧、表示、実演、Forkによる複製等を許可するライセンスが発生する。追加の権利は別途ライセンスで与えることができる。

したがって、現在の **All Rights Reserved** は概ね妥当だが、厳密には「GitHub Termsにより必要な範囲の権利を除き、追加の一般利用許諾はしていない」という状態。

### 評価

**Medium wording risk, not an emergency**

`RIGHTS.md` の趣旨と大きな矛盾はない。ただし将来の誤解を減らすなら、一文だけ補足してもよい。

例:

> Public availability on GitHub does not by itself grant an open-content license beyond the rights necessary to use GitHub's service features under GitHub's Terms of Service.

公式資料:

- GitHub Terms of Service: https://docs.github.com/en/site-policy/github-terms/github-terms-of-service
- GitHub Docs「Licensing a repository」: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository

## 5. READMEの「Open Story IP」表現

現在のREADMEは、オープン化が将来構想であることを複数箇所で明記しており、全体としては誤認防止ができている。

ただし次のコピーは単独で切り取ると、現時点ですでに派生利用を許諾しているようにも読める。

> Read it. Fork it. Build your own branch.

直後に「現時点ではまだオープンライセンスへの移行前」と書かれているため重大ではないが、SNSや検索結果等で一部だけ引用される可能性を考えると、将来的には `Future vision:` 等を付けるか、オープン化後に本格利用するコピーとして予約する方法もある。

### 評価

**Medium / documentation clarity**

## 6. AI利用と著作権

文化庁の「AIと著作権に関する考え方について」は、AI学習・生成のすべてを一律にライセンス問題として扱っていない。

日本の著作権法第30条の4等の権利制限が適用され、許諾を要しない利用であれば、CCライセンスを付けていても、その利用をCC条件で拘束するわけではない。Creative Commonsのリーガルコード自体も、権利制限が適用される利用についてCC条件への遵守は不要としている。

また文化庁は、AI生成物の著作物性について、人の創作意図と創作的寄与を総合的に判断する必要があると説明している。

したがって将来の説明では、

- 「CC BY-SAだからAI学習は可能」
- 「AIが使ったら必ずShareAlikeになる」

のような単純化は避ける。

### 評価

**Low now / Medium for future guidance**

公式資料:

- 文化庁「AIと著作権について」: https://www.bunka.go.jp/seisaku/chosakuken/aiandcopyright.html
- 「AIと著作権に関する考え方について」令和6年3月15日
- 文化庁FAQ: https://www.bunka.go.jp/seisaku/chosakuken/kaizoku/faq.html

2026年時点でも政府はAI時代の知財保護・透明性について追加検討を進めており、今後制度・実務が更新される可能性が高い。ライセンス発動時には最新状況を再確認する。

## 7. 外部Contribution

現時点のリポジトリには `CONTRIBUTING.md` がなく、第三者の創作的Contributionを受け入れる権利処理ルールもまだない。

GitHub Termsでは、ライセンス表示のあるrepositoryへContentを追加すると、原則そのrepositoryのライセンス条件でContributionする仕組みがある。しかし、Moonnet Sagaのように「Canon採用」「再ライセンス」「将来の商用利用」「著作者人格権」「作品単位でライセンス範囲を変える」可能性があるプロジェクトでは、GitHub Termsだけに依存せず、Contributor向けルールを明示する方がよい。

### 外部Contribution開始前に決めること

- PRで受け付ける対象（誤字修正／設定／物語／画像等）
- 投稿者が必要な権利を有することの表明
- Contributionに適用されるライセンス
- Canon採用の有無とは無関係であること
- クレジット方法
- 第三者素材の禁止または表示方法
- 必要ならCLAを採用するか

### 評価

**Medium before accepting creative PRs**

当面、外部から創作本文や設定のPRを積極募集しないなら緊急ではない。

## 8. 著作者人格権

日本の著作権法では著作者人格権は著作者に一身専属し、譲渡できない。CC BY-SA 4.0も人格権そのものを移転するものではなく、許諾された利用に必要な限定範囲について可能な限り不行使等を規定する。

Moonnet Sagaでは、第三者が原作と大きく異なる価値観・成人向け・政治的・宗教的表現等を含むbranchを作る可能性をREADMEに明記している。この方向性自体はCCの`No endorsement`とも整合するが、将来実際にオープン化する際には、作者が「どこまでの改変を許容するか」ではなく、**CC BY-SAが許す改変を理解した上で採用する**必要がある。

### 評価

**Medium / author decision before activation**

## 9. 商標・名称

### 調査結果

通常のWeb検索では、2026-08-29時点で「Moonnet Saga」「ムーンネットサーガ」について同一の著名サービス・作品シリーズは確認できなかった。

一方、`MOONNET` / `ムーンネット` 単独では、国内外で会社名・商品名・技術名等として利用例が存在する。このため「Moonnet」という語だけを独占できる、または安全に登録できるとは判断できない。

J-PlatPatの商標検索画面自体は確認できたが、この調査環境から動的検索結果を信頼できる形で取得できなかったため、**正式な先行商標検索は未完了**。

### 評価

**Low now / Medium before branding investment or trademark filing**

### 推奨

J-PlatPatで少なくとも以下を検索する。

- Moonnet Saga
- MOONNET SAGA
- ムーンネットサーガ
- Moonnet
- ムーンネット
- Open Story IP

文字列完全一致だけでなく、称呼（類似検索）を使い、想定する商品・役務区分を確認する。

特許庁案内:

- https://www.jpo.go.jp/support/startup/shohyo_search.html
- J-PlatPat: https://www.j-platpat.inpit.go.jp/

## 10. 第三者素材・引用

公開中の本文について、今回の調査では全文を一文ずつ既存著作物と照合するフォレンジックな引用監査は行っていない。

将来CC化する版については、次を作品単位で確認する。

- 歌詞・詩・小説等からの引用
- 他者の写真、イラスト、地図
- 表紙・装丁
- 編集者・共同作者による創作的文章
- 実在人物の写真・肖像・プライバシー情報
- 第三者が権利を持つ翻訳

単なる商品名・地名・一般的な固有名詞の登場だけを理由に除外する必要はないが、第三者著作物そのものを含む部分は別管理する。

### 評価

**Medium before CC activation**

## 11. 現状で直すべきか

### すぐ人間が確認すべき

1. KDP Selectの現在の登録状態
2. オルタニア掲載時の契約・募集要項・メール等の所在

### 文書として直すとよいが緊急ではない

1. GitHub TermsによるFork等の扱いをRIGHTSに一文追記
2. `Read it. Fork it. Build your own branch.` を将来構想とより明確に紐付ける
3. 外部Contribution開始前に `CONTRIBUTING.md` を用意

### 今はしない

- repository全体への `LICENSE` 追加
- CC BY-SA 4.0の発効
- `possible`作品を自動的にCC対象とすること
- 契約未確認作品のオープン化

## 12. 推奨ゲート

CC BY-SA 4.0を実際に発効する前に、以下の全条件を満たす。

- [ ] 対象作品の著作権・出版権・独占許諾を確認済み
- [ ] KDP Select等の独占条件と衝突しない
- [ ] 対象版を特定済み
- [ ] 第三者素材を除外または別ライセンス表示済み
- [ ] 作者が取消不能・商用利用・翻案・ShareAlikeを理解して選択済み
- [ ] Canon statusとlicense statusを別表示
- [ ] 商標はCC対象外と明記
- [ ] attributionの推奨形式を用意
- [ ] Contribution方針を決定
- [ ] `RIGHTS.md` / README / 各作品READMEの表示が一致
- [ ] 発効直前に最新の法制度・CC文面・配信契約を再確認

## Sources

一次資料・公式資料を優先した。

- e-Gov 著作権法: https://laws.e-gov.go.jp/law/345AC0000000048
- 文化庁「AIと著作権について」: https://www.bunka.go.jp/seisaku/chosakuken/aiandcopyright.html
- 文化庁「AIと著作権に関する考え方について」関連資料: https://www.bunka.go.jp/seisaku/bunkashingikai/chosakuken/hokoku.html
- Creative Commons BY-SA 4.0 Legal Code (JA): https://creativecommons.org/licenses/by-sa/4.0/legalcode.ja
- Creative Commons BY-SA 4.0 Legal Code (EN): https://creativecommons.org/licenses/by-sa/4.0/legalcode.en
- GitHub Terms of Service: https://docs.github.com/en/site-policy/github-terms/github-terms-of-service
- GitHub Licensing a repository: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository
- Amazon KDP Select: https://kdp.amazon.co.jp/ja_JP/select
- Amazon KDP Select requirements: https://kdp.amazon.co.jp/ja_JP/help/topic/GD9PMU58BV24QFZ7
- 特許庁「商標を検索してみましょう」: https://www.jpo.go.jp/support/startup/shohyo_search.html

補助的な公開確認:

- BCCKS オルタニア vol.7: https://bccks.jp/bcck/157010/info
- BOOK☆WALKER オルタニア vol.7: https://bookwalker.jp/de0e074d1c-a6ac-4607-9f2c-279f2c1262e2/

## 調査上の限界

- 非公開の出版契約書・メール・KDP管理画面は確認していない。
- J-PlatPatの正式な類似商標検索結果は取得できていない。
- 各小説本文について、第三者著作物との逐語的な網羅照合はしていない。
- 海外各国の著作権法を国別に精査していない。

したがって、最も重要な次の一手は**ライセンス変更ではなく、KDP状態と過去契約の事実確認**である。
