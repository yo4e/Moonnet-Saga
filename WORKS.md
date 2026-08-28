# Works

Moonnet Saga の作品カタログ。

詳細な世界設定・技術・年代・人物関係など、作品から抽出した観測事項は [`world/works/`](world/works/) に分離して記録します。

## Saga status

作品とMoonnet Sagaの関係は、次の3分類で扱います。

- `confirmed` — 確実にMoonnet Saga
- `possible` — Moonnet Sagaかもしれない／作者記憶や作品上の接続可能性がある
- `excluded` — 確実にMoonnet Sagaではない
- `—` — まだ分類していない。4つ目の分類ではなく未判定状態

**`confirmed` と `possible` の作品本文は、権利・版を確認できたものから `works/` に収録します。** `possible` のまま収録してかまいません。

作品をこのリポジトリへ収録すること、公式Canonとすること、CC BY-SA等のオープンライセンス対象とすることは、それぞれ別の判断です。

## 作品一覧

|作品|Saga status|本文|初出・状態|権利|
|---|---|---|---|---|
|アンフォールドザワールド|`possible`|未収録|SF雑誌「ガンズ」|All Rights Reserved|
|暁の夜|`confirmed`|未収録|未完稿|All Rights Reserved|
|ボタニカルアリス|`confirmed`|未収録|確認中|All Rights Reserved|
|十＋十|`possible`|未収録|執筆中|All Rights Reserved|
|マイニングファームにて|`possible`|[読む](works/mining-farm-nite/)|初出確認中|All Rights Reserved|
|アウトサイドフィールズ|`possible`|未収録|SF雑誌オルタニア Vol.18（2022）|All Rights Reserved|
|いいじいえいあい|`possible`|未収録|SF雑誌オルタニア 増刊号 vol.9.999（2021）|All Rights Reserved|
|砂糖楓|—|未収録|てきすぽどーじん6号（2013）|All Rights Reserved|
|タカシ|`confirmed`|[読む](works/takashi/)|SF雑誌オルタニア vol.7［後継種］（2018）|All Rights Reserved|
|虚偽記憶の共犯者|—|未収録|SF雑誌オルタニア バイキング増刊号9.5（2020）|All Rights Reserved|
|おとなになれないきみたちとふたたび|—|未収録|SF雑誌オルタニア vol.7.5（2019）|All Rights Reserved|
|昂奮ブロマイド|—|未収録|SF雑誌オルタニア vol.6（2018）|All Rights Reserved|
|ワンダリングリング|`possible`|未収録|『ワンダリングリング 山田佳江SF短編集』（2022）書き下ろし|All Rights Reserved|

## 公開作品のディレクトリ形式

作品本文を収録する場合は、原則として次の形にします。

```text
works/<slug>/
├─ README.md   # 作品の公開メタデータ／入口
├─ text.md     # 現在公開する本文
└─ editions/   # 別版が必要になった場合のみ追加
```

`README.md` には、著者、Saga status、初出、収録、公開・販売先、権利状態など、公開に必要な最小限の書誌情報を置きます。本文とメタデータを分けることで、書誌情報の更新や別版追加のたびに本文全体を書き換えずに済むようにします。

## 運用

- Yoshie Yamada Corpus で作品を収集・確認する。
- Saga status が `confirmed` または `possible` で、公開に必要な権利・版を確認できた作品は、このリポジトリの `works/` にコピーする。
- 初出、収録、公開・販売先などの公開書誌情報は、各作品の `README.md` に記載する。
- Corpus内部の正本、転記元、ハッシュ、Googleドキュメント等の保存情報は、この公開リポジトリには持ち込まない。
- 権利状態は作品ごとに明示する。現時点ではすべて All Rights Reserved であり、CC BY-SA等への移行は別途明示した作品だけを対象とする。
