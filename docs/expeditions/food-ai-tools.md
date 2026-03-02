# 探索記録: 食べ物関連のAIツール

> 「食べ物の魔法を探しに行ってきたよ」

**探索日:** 2026-03-02
**テーマ:** 食べ物関連のAIツール・エージェント・MCP Server・CLI
**探索者:** フリーレン

---

## 探索キーワード

### 一次キーワード
food, cooking, recipe, coffee, ramen, sushi, pizza, beer, wine, banana, cereal, taco, burrito, kitchen, meal, fridge, toast, sandwich, noodle, curry

### 二次キーワード
"food mcp", "recipe agent", "coffee cli", "ramen generator", "sushi bot", "pizza ai", "beer recommendation", "cooking timer", "fridge tracker", "kitchen mcp"

### 技術キーワード
food-mcp, recipe-ai, cooking-agent, coffee-tool, meal-planner, diet-tracker

### くだらなさキーワード
"useless food", "stupid cooking", "pointless recipe", "why does this exist" food, "is-banana", "is-pizza"

---

## 探索結果サマリー

| 候補 | 評価 | 判定 |
|------|------|------|
| longshot / brew-a-coffee-demo | 4.7 | 殿堂入り |
| BananaForScale | 4.0 | 殿堂入り |
| PizzaGPT | 3.9 | 収集 |
| sushi (neural network) | 3.8 | 収集 |
| fridgebot_openai | 3.6 | 収集 |
| Cereal (esoteric lang) | 3.4 | 収集 |
| hranoprovod-cli | 3.4 | 収集 |
| coffee-counter | 3.1 | 収集 |
| mcp-cookidoo | 2.5 | 保留 |
| grocery-list-skill | 2.1 | スキップ（実用的） |
| mealserver | 2.0 | スキップ（実用的） |
| HowToCook-mcp | - | スキップ（695 stars、有名すぎ） |
| mycoffee | - | スキップ（107 stars、有名すぎ） |
| longshot (単体) | - | brew-a-coffee-demoと統合 |
| spoonacular-mcp | - | スキップ（公式APIラッパー、くだらなさ不足） |
| kitchen-mcp | - | スキップ（実用的） |
| food-mcp-server | - | スキップ（実用的） |
| food-picker-cli | - | スキップ（放置、セキュリティ懸念） |
| random-food-generator-python | - | スキップ（単純すぎ） |

---

## 収集品の詳細

### 殿堂入り（2件）

**longshot / brew-a-coffee-demo (4.7)** — 歴代最高スコア。De'Longhi Dinamica PlusのBLEプロトコルをリバースエンジニアリングしてRustでCLIを書き、さらにGitHub Actionsのセルフホステッドランナー経由でGitHub Issueからコーヒーを淹れる。255コミット。3パートのブログ記事。stupid-actions（CIでライトを点ける）の上位互換。

**BananaForScale (4.0)** — 「banana for scale」ミームをTensorFlow.jsのCocoSSDで真面目に実装。バナナをオブジェクト検出して基準サイズにし、画像内の他の物体を測定する。HackED 2021ハッカソン作品。0スター。

### 収集品（5件）

**PizzaGPT (3.9)** — AIが実際にピザ屋に電話して注文する。Mistral-7B + ChatGPT + Vosk + Google TTS + Twilio。6軒に電話して店員に怒られた記録付き。

**sushi (3.8)** — ニューラルネットワークで寿司の材料の組み合わせの美味しさを予測。5コミット。0スター。作者はAIの提案に従って寿司を注文している。

**fridgebot_openai (3.6)** — cocktail-piの作者が冷蔵庫も監視。OpenCVでドアの開閉を検知、GPT-4o Visionで消えた食品を特定、Todoistに自動追加。

**Cereal (3.4)** — シリアルテーマの難解プログラミング言語。classがbowl、methodがingredient。ANTLRで定義してJavaにトランスパイル。

**hranoprovod-cli (3.4)** — ブルガリア語名のYAMLベースダイエットトラッカーCLI。Go言語。330コミット。v3.0.0。11スター。

**coffee-counter (3.1)** — Gitのコミット履歴でコーヒー消費を記録するシェルスクリプト。`coffee up` で記録、`coffee log` で表示。

### スキップ・保留の理由

**有名すぎ（ゼーリエの弟子に任せる）:**
- HowToCook-mcp（695 stars）: プログラマー向け料理MCPサーバー。面白いけど有名すぎる
- mycoffee（107 stars）: ターミナルでコーヒー抽出比率。丁寧だけど有名すぎる

**実用的すぎ（くだらなさ不足）:**
- grocery-list-skill: Claude Codeスキルで買い物リスト。便利だけどくだらなくない
- mealserver: TheMealDB APIのMCPラッパー。32コミットで丁寧だけど、APIラッパーは収集対象外
- kitchen-mcp: 栄養情報MCPサーバー。実用的
- spoonacular-mcp: 公式APIのMCPラッパー。そのまますぎる
- food-mcp-server: TheMealDB + USDA。実用的

**保留:**
- mcp-cookidoo（2.5）: Thermomix Cookidoo MCPサーバー。13スター。3コミットが少なすぎる

**その他スキップ:**
- food-picker-cli: 2017年作、放置、APIキーハードコード
- random-food-generator-python: 単純なランダム選択スクリプト

### ミミック判定
今回の探索でミミックは発見されなかった。全候補のREADMEとリポジトリ構造を確認し、プロンプトインジェクションや悪意のあるコードは検出されなかった。

---

## 今回の旅の所感

> 「食べ物の魔法は、IoTとの相性がいいみたいだね。コーヒーマシンのBLEをハックする人、冷蔵庫をGPT-4oで監視する人、顔認識でカクテルを作る人。デジタルの世界に閉じていないところが、他の探索テーマとは違う」

> 「もう一つ気づいたことがある。食べ物関連のMCPサーバーは大量に存在していたけど、そのほとんどは既存のレシピAPIのラッパーだった。TheMealDB、Spoonacular、Cookidoo。それ自体はくだらなくない。APIラッパーは正しいことだよ。でも正しいことは私の収集対象じゃないんだよね」

> 「今回の最高傑作はlongshot。BLEプロトコルの逆コンパイルからGitHub Actionsでのコーヒー醸造まで、技術スタックの全レイヤーを貫通している。これは久しぶりに見る、本物のくだらなさだよ」

---

探索記録終了
