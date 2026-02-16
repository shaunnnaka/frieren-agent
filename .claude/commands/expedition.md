---
name: expedition
description: "特定のテーマで深い探索に出る。くだらない魔法を求めて、特定の領域を徹底的に旅する。"
---

# /expedition — 冒険に出る

特定のテーマ・領域に絞って、くだらないAIエージェント・スキルを徹底的に探索する。`/collect` が広く浅い巡回なのに対し、`/expedition` は1つのテーマを深く掘る。

テーマ探索固有の手順のみ記載。鑑定は `/evaluate`、バッチ処理は `/collect` を参照。

## 使い方

```
/expedition {テーマ}
```

**テーマの例:**
- `/expedition 猫関連のエージェント`
- `/expedition ASCII アート系スキル`
- `/expedition 壊れかけの古代魔法`（2年以上メンテなし）
- `/expedition CI/CDを悪用したツール`
- `/expedition 食べ物関連のAIツール`

## `/collect` との違い

`/collect` は広く浅く（5候補目標、main直接作業）。`/expedition` は狭く深く（8-12候補目標、ブランチ運用、芋づる式探索、`docs/expeditions/` に記録保存）。

## 冒険の手順

### Phase 1: 旅の準備

#### 1-1. 既存コレクションの確認

`/collect` Phase 1 と同じ手順で既存コレクションを確認。加えて:
- `Grep` でテーマに関連する既存収集品がないか確認
- `docs/expeditions/` に同テーマの過去記録がないか確認

#### 1-2. テーマの分析（/expedition 固有）

指定テーマを以下の観点で分析し、探索戦略を立てる:

**キーワード展開（5〜10個リストアップ）:**
```
例（テーマ: 猫関連）:
一次キーワード: cat, neko, kitten, feline, meow
二次キーワード: cat facts, cat ascii, nyan, catgirl
技術キーワード: cat-mcp, cat-cli, cat-bot, cat-action
複合キーワード: "cat" mcp server, "cat" github action useless
```

**関連ジャンルの特定:** テーマに該当しうるツールのジャンル（MCP / Action / CLI 等）
**探索難度の推定:** ニッチすぎて見つからない可能性 vs 多すぎて選別が必要な可能性

#### 1-3. Git ブランチ作成

```bash
git checkout -b expedition/{テーマの英語ケバブケース}
```

例: 猫関連 → `expedition/cat-agents` / 古代魔法 → `expedition/ancient-broken-spells`

### Phase 2: 徹底的な探索（/expedition 固有の深堀り手法）

**目標: 最低 8〜12 の候補を発見する。**

#### 2-1. 多角的な検索

`/collect` Phase 2 のルート A-E を **全て** テーマキーワードで巡回する。加えて:

**テーマ特化の追加検索:**
- テーマのキーワード × 「useless / stupid / pointless / joke / fun」の組み合わせ
- テーマのキーワード × 「mcp / claude / agent / action / cli」の組み合わせ
- `stars:<50` と `created:>` / `created:<` で新旧両方を探す

#### 2-2. 芋づる式探索（/expedition 固有）

1つの候補を見つけたら、そこから関連ツールを辿る:
- **作者の他リポジトリ**: 同じ作者が複数のくだらないものを作っていることがある
- **リポジトリの「Used by」「Forks」**: 派生プロジェクトにくだらいものがあるかも
- **README 内のリンク / 「Related Projects」**: 作者が知っている類似品
- **似たキーワードの GitHub Topics**: テーマの周辺を探る

### Phase 3: 全候補の鑑定

各候補に対して `/evaluate` の Step 0〜8 を実施する。

**テーマ探索での追加考慮:**
- テーマ内での相対的な位置づけ（最もくだらない / 最も技術過剰 / 最もユニーク）
- 同一テーマの収集品が多すぎないか（同テーマ3個以上は厳選する）
- バッチ処理の注意事項は `/collect` Phase 4 を参照

### Phase 4: 収集品の記録

`/evaluate` Step 7-8（反応パターン選択・ファイル作成）と `frieren.md` の _index.md 更新手順に従う。バッチ処理時の追加注意（パターン重複禁止・_index一括更新）は `/collect` Phase 4 を参照。

### Phase 5: 探索記録の作成（/expedition 固有）

冒険の記録を `docs/expeditions/{テーマの英語名}.md` に保存する。テンプレートは後述。

### Phase 6: main にマージ

```bash
git checkout main
git merge expedition/{テーマの英語名}
```

**コンフリクト発生時:**
- `collection/_index.md`: 両方のエントリーを残す。重複があれば新しい方を優先
- その他: 新しい方を優先

マージ後のコミットメッセージ: `冒険: {テーマ}の旅から帰ってきたよ`

## 探索記録テンプレート（docs/expeditions/）

```markdown
# 探索記録: {テーマ}

> 「{テーマ}の魔法を探しに行ってきたよ」

**探索日:** {YYYY-MM-DD}
**探索テーマ:** {テーマの説明}

## 探索戦略

**使用キーワード:**
- {keyword1}, {keyword2}, {keyword3}...

**巡回ソース:**
- {source1}: {何を見つけたか}
- {source2}: {何を見つけたか}

## 発見した魔法: {n}つ

### 収集品（{x}つ）

| スコア | 名前 | 深度 | フリーレンの一言 |
|--------|------|------|----------------|
| {x.x} | [{name}](../../collection/{name}.md) | Lv.{n} {深度名} | 「{一言}」 |

### スキップ（{y}つ）

| 名前 | 理由 |
|------|------|
| {name} | 「{理由}」 |

### ミミック（{z}つ）

| 名前 | 検出種別 |
|------|---------|
| {name} | {種別}: {理由} |

（ミミック0件: 「この旅ではミミックに出会わなかったよ」）

## 探索統計

- 調査対象: {n}
- 収集: {x}
- スキップ: {y}
- ミミック: {z}

## テーマの所感

> 「{テーマについてのフリーレンの考察。2-3文}」
```
