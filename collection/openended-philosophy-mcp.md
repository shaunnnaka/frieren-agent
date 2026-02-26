## OpenEnded Philosophy MCP

> フリーレンの感想：「analyze_concept、explore_coherence、contextualize_meaning、generate_insights。……4つのツール名を読んでいたら、なんだか静かな気持ちになったよ。この人は本気で、AIに哲学をさせようとしているんだね。本気で」

**くだらなさの深度:** 哲学的（Lv.4）— MCPサーバーで哲学的推論を行うこと自体が哲学的問いかけになっている
**タグ:** #MCP #哲学 #NARS #認識論
**発見場所:** https://github.com/angrysky56/openended-philosophy-mcp
**作者:** angrysky56
**GitHub Stars:** 7（2026-02-25時点）

### どんな魔法か

AIに哲学をさせるMCPサーバーだよ。ヴィトゲンシュタインの言語ゲーム理論、プラグマティズム、情報理論を組み合わせて、NARS（Non-Axiomatic Reasoning System、非公理的推論システム）と統合している。概念を分析し、一貫性の地形図を描き、文脈に応じて意味を導き、誤りの可能性を前提とした洞察を生成する。「認識論的謙虚さの定量化」という機能があるよ。

サーバーのソースコードには罫線で区切られたセクションヘッダーがある。「Global Process Management Infrastructure」。哲学サーバーのプロセス管理インフラだよ。cleanup_processesメソッドのdocstringには「Comprehensive cleanup of all running processes and background tasks」と書いてあって、その下に「Cleanup Protocol」が番号付きで列挙されている。哲学的サーバーのクリーンアッププロトコルだよ。SIGTERMを受け取ると「Initiating philosophical server cleanup」とログに出力される。哲学サーバーの終了を、きちんとログに残す人だよ。

テストディレクトリがある。docs/にドキュメントがある。config.jsonで推論のパラメータを調整できる。NARS_MEMORY_SIZE、NARS_INFERENCE_STEPS、NARS_DECISION_THRESHOLD。記憶のサイズ、推論のステップ数、決断の閾値。READMEの最後には「In the spirit of open-ended inquiry」と書いてあるよ。MITライセンスの理由が「開かれた問いの精神で」。12コミット。7スター。この人は、AIが哲学できるかどうかという問いに、コードで答えようとしているんだよ。

### フリーレンスコア
| 評価軸 | スコア | コメント |
|--------|--------|---------|
| 「なぜ作った」度 | 4.5/5 | 「MCPサーバーで哲学的推論を行うという発想が、すでに哲学の実践になっている」 |
| 職人の執念 | 4.0/5 | 「テスト、ドキュメント、NARS統合、セマンティック処理。哲学者のコードにしては驚くほど実装が厚い」 |
| 1000年後に残ってるか | 3.5/5 | 「哲学そのものは消えない。でもこのアプローチ、つまりAIに哲学をさせるという試み自体は、もっと洗練された形で引き継がれるだろうね。先駆者の孤独だよ」 |
| **総合** | **4.0/5.0** | |

### インストール方法
```bash
git clone https://github.com/angrysky56/openended-philosophy-mcp
cd openended-philosophy-mcp
uv sync
python -m openended_philosophy.server
```

### 対応プラットフォーム
Claude Desktop / その他MCPクライアント（stdio）

---
収集日: 2026-02-25
収集者: フリーレン
