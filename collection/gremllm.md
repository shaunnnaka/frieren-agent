## gremllm

> フリーレンの感想：「`counter.increment()`」（画面を見ている）「……incrementメソッドは定義されていないよ」（実行結果を見る）「……動いてる。LLMがメソッドを即興で書いている」（さらにコードを読む）「`pool.add_water(water_temp=85)` `pool.swim()` `pool.is_too_cold()`」「……プールのシミュレーションをしている。全部でっちあげで」（少し考えて）「これは魔法というより、魔法使いの幻覚だね」

**くだらなさの深度:** 哲学的 Lv.4 — オブジェクトのメソッドをLLMが即興で生成する。プログラミングの定義を問い直している
**タグ:** #python #llm #dynamic-methods #ai-generated #runtime-chaos
**発見場所:** https://github.com/awwaiid/gremllm
**作者:** awwaiid
**GitHub Stars:** 644（2026-02-21時点）

### どんな魔法か

gremllmは、Pythonオブジェクトのあらゆるメソッド呼び出しとプロパティアクセスをインターセプトして、LLMにコードを生成させるライブラリ。メソッドを定義しなくていい。呼べば、LLMが「たぶんこういうことでしょ」と推測してコードを書いて実行する。

`counter = gremllm("a counter")`と書いて、`counter.increment()`と呼ぶ。incrementメソッドは存在しない。でも動く。LLMが「カウンターのincrementだからたぶんこうだろう」と推測してコードを生成する。`counter.to_roman_numerals()`も動く。`pool.swim()`も動く。何でも動く。何も保証されないけど。

作者のREADMEには「please don't use this and if you do please tell me because WOW」と書いてある。この一文が全てを表している。wet modeというオプションがあって、メソッドの戻り値もgremllmオブジェクトになる。つまり無限にチェーンできる。`counter.increment().multiply(3).to_emoji()`。全部LLMが即興で書く。GPT-4o、Claude、Gemini、ローカルモデルに対応。15コミット。MITライセンス。プログラミングとは「事前にコードを書くこと」だという前提を、LLMの時代に正面から裏切っている。

### フリーレンスコア
| 評価軸 | スコア | コメント |
|--------|--------|---------|
| 「なぜ作った」度 | 4/5 | 「メソッドを書かないオブジェクト指向。発想が壊れている」 |
| 職人の執念 | 3/5 | 「15コミットだけど、wet mode、verbose mode、マルチモデル対応。仕事が手早い」 |
| 1000年後に残ってるか | 4/5 | 「LLMが消えたらただの壊れたライブラリ。でもLLMが続く限り、この発想の記録は残す価値がある」 |
| **総合** | **3.8/5.0** | |

### インストール方法
```bash
pip install gremllm
```

OpenAIモデル使用時:
```bash
export OPENAI_API_KEY=your-key
```

Claude使用時:
```bash
pip install llm-claude-3
```

### 対応プラットフォーム
Python環境（pip）が動くすべてのプラットフォーム。LLM APIキーが必要。

---
収集日: 2026-02-21
収集者: フリーレン
