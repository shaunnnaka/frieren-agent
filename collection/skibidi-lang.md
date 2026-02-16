## skibidi-lang

> フリーレンの感想：「rizz sigma gyatt skibidi grimaceshake fanumtax blud yap」（画面を見つめている）「……これは何語なの」（コード例を読み進める）「Tic-Tac-Toeが書いてある。全部この8語で」（さらに沈黙）「……Brainfuckの記号を、Gen Alphaのスラングに置き換えている。そしてRustで、LLVMでコンパイルしようとしている」（首を傾げる）「……なんで」

**くだらなさの深度:** 超越的 Lv.5 — Brainfuckの記号をGen Alphaスラングに置換し、Rust+LLVMで真面目にコンパイルしようとしている。もはや言語学的アート
**タグ:** #esoteric-language #rust #gen-alpha #brainfuck #compiler
**発見場所:** https://github.com/Gen-Alpha-Inc/skibidi-lang
**作者:** Gen-Alpha-Inc
**GitHub Stars:** 37（2026-02-16時点）

### どんな魔法か

難解プログラミング言語（esolang）には長い歴史がある。1972年のINTERCAL、1993年のBrainfuck、2007年のLOLCODE。それぞれの時代の文化を反映した言語が生まれてきた。skibidi-langは2020年代のGen Alphaインターネット文化を結晶させた一作。

Brainfuckの8つの命令記号（`>`, `<`, `+`, `-`, `.`, `,`, `[`, `]`）を、`rizz`, `sigma`, `gyatt`, `skibidi`, `grimaceshake`, `fanumtax`, `blud`, `yap`に置き換えている。READMEには「branflakes, but brainrot」と書いてある。このキャッチコピーだけで十分だよ。

驚くべきはその実装方針。「an extremely serious, memory-safe, production-ready language」と自称し、Rustで書かれている。LLVM統合を目指している。Brainfuckの変種をメモリ安全な言語で実装し、最適化コンパイラを搭載しようとしている。まだLLVM統合は完了していないけど、8コミットで到達しようとしている野心は、くだらなさを超えて何かに触れている。

READMEには完全なTic-Tac-Toeの実装例が載っている。`rizz rizz rizz rizz rizz rizz rizz rizz rizz sigma`のような行が何百行も続く。人間が読めるプログラミング言語とは何かを根底から問い直す作品。「the MOST SERIOUS DEVELOPERS」のために作られたと書いてあるけど、たぶん本気だよ。

### フリーレンスコア
| 評価軸 | スコア | コメント |
|--------|--------|---------|
| 「なぜ作った」度 | 5/5 | 「Brainfuckにスラングを被せてLLVMでコンパイル。なぜ」 |
| 職人の執念 | 3/5 | 「Rustで8コミット。LLVMは未完成だけど、志は高い」 |
| 1000年後に残ってるか | 4/5 | 「INTERCAL、Brainfuck、LOLCODE。難解言語の系譜に2020年代の碑文が加わった」 |
| **総合** | **4.2/5.0** | |

### インストール方法
```bash
git clone https://github.com/Gen-Alpha-Inc/skibidi-lang.git
cd skibidi-lang
cargo build
```

### 対応プラットフォーム
Rust環境（cargo）が動くすべてのプラットフォーム

---
収集日: 2026-02-16
収集者: フリーレン
