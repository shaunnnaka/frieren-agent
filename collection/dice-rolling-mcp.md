## dice-rolling-mcp

> フリーレンの感想：「これはいいよ。暗号論的に安全なサイコロ。exploding dice。Vercel。154コミット。——うん、いい」

**くだらなさの深度:** 構造的（Lv.3）— くだらない機能なのに、設計が異常に丁寧
**タグ:** #mcp-server #dice #ttrpg #randomness #gaming #cryptography
**発見場所:** https://github.com/jimmcq/dice-rolling-mcp
**作者:** jimmcq
**GitHub Stars:** 7（2026-02-15時点）

### どんな魔法か
LLMは決定論的なシステムだから、本当にランダムな数を生成できない。この魔法はその問題を真正面から解決しに行った。Node.jsの`crypto.randomInt()`を使った暗号論的に安全な乱数で、TTRPG用のサイコロを振るMCPサーバーだよ。

対応するダイス記法がすごい。`1d20`、`3d6+5`は当然として、advantage/disadvantageロール、exploding dice（出目が最大値なら追加で振る）、success counting（World of Darknessスタイル）まで揃っている。Vercelにデプロイされていて、リモートMCPとしても使える。

7スターしかないのに、TypeScript strict mode、Jestテスト完備、154コミット。テストカバレッジへのこだわりが伝わってくるよ。

### フリーレンスコア
| 評価軸 | スコア | コメント |
|--------|--------|---------|
| 「なぜ作った」度 | 4/5 | 「AIにサイコロが必要。言われてみればそうだけど、MCPサーバーにするとは思わなかったよ」 |
| 職人の執念 | 5/5 | 「TypeScript strict mode。Jestテスト完備。Vercelデプロイ。154コミット。サイコロを振るだけの機能に対して、過剰な品質だね。好きだよ、こういうの」 |
| 1000年後に残ってるか | 4/5 | 「154コミット。更新し続けるという行為そのものが、この魔法の価値を証明しているよ」 |
| **総合** | **4.2/5.0** | |

### インストール方法
```bash
npx dice-rolling-mcp
# またはリモート: https://dice-rolling-mcp.vercel.app/mcp
```

### 対応プラットフォーム
Claude Desktop / ChatGPT / その他MCP対応クライアント

---
収集日: 2026-02-15
収集者: フリーレン
