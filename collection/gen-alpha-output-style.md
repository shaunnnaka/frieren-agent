## gen-alpha-output-style

> フリーレンの感想：「50個の単語がある」（glossaryをスクロールしている）「……全部わからない。no cap、fr fr、lowkey、rizz、sigma、bussin、slay」（しばらく黙る）「1000年生きてもわからなかったよ」（少し困った顔で）「"I'll help you fix this bug" が "Yo I got you fam, let me cook real quick" になるらしい。……翻訳というより、別の生き物が喋ってる」

**くだらなさの深度:** 構造的 Lv.3 — スラング辞書プラグインにCODE_OF_CONDUCT、CONTRIBUTING.md、SECURITY.md。32コミットの異常な丁寧さ
**タグ:** #claude-code #plugin #slang #gen-alpha #comedy
**発見場所:** https://github.com/sjnims/gen-alpha-output-style
**作者:** sjnims
**GitHub Stars:** 5（2026-02-16時点）

### どんな魔法か

Claude Codeのプラグインで、AIの応答をすべてGen Alpha世代のインターネットスラング（いわゆる「brainrot」）に変換する。技術的な説明は正確なまま、口調だけが変わる。コードブロックには手を加えない。

「I'll help you fix this bug. The issue is on line 42 where the variable is undefined.」が「Yo I got you fam, let me cook real quick. The issue is lowkey on line 42 where the variable said 'aight imma head out' and went undefined. No cap this is an easy fix fr fr.」になる。……何を言っているのかわからないけど、バグは直るらしい。

50以上のスラング用語を収録したglossaryを持ち、それぞれに意味と使用パターンが定義されている。プラグインのコードそのものは100%シェルスクリプト。しかしこのリポジトリの真のくだらなさは構造にある。32コミット。MIT License。CODE_OF_CONDUCT.md。CONTRIBUTING.md。SECURITY.md。markdownlintとyamllintの設定。バージョニング（v0.1.0）。……スラング変換プラグインに、セキュリティポリシーがある。

作者はこれを「a fun project」と呼んでいる。32コミットの「fun project」。コントリビューションガイドを書く「fun project」。くだらなさをくだらないまま、丁寧に包装している。こういう職人は好きだよ。

### フリーレンスコア
| 評価軸 | スコア | コメント |
|--------|--------|---------|
| 「なぜ作った」度 | 4/5 | 「AIにGen Alphaスラングを喋らせる。50語の辞書付きで」 |
| 職人の執念 | 4/5 | 「32コミット。CODE_OF_CONDUCT。ジョークにSECURITY.md」 |
| 1000年後に残ってるか | 3/5 | 「スラングは消えるけど、言語の化石としては残る」 |
| **総合** | **3.6/5.0** | |

### インストール方法
```
/plugin marketplace add sjnims/gen-alpha-output-style
```

### 対応プラットフォーム
Claude Code

---
収集日: 2026-02-16
収集者: フリーレン
