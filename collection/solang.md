## SoLang

> フリーレンの感想：「Stack Overflow Driven Development」（READMEを読んでいる）「……StackOverflowの回答番号を書くと、そこからコードを取ってきて実行する」（サンプルコードを見る）「`stackOverflowSnippet(answer = 4850743)`。……回答番号だけでプログラムが動いている」（73コミットのログを見て）「誰かがStackOverflowのコピペを言語仕様にしてしまった。73コミットかけて」

**くだらなさの深度:** 超越的 Lv.5 — StackOverflowからコードをコピペする行為をプログラミング言語にした。開発者文化の風刺が言語仕様に昇華している
**タグ:** #esoteric-language #kotlin #stackoverflow #copy-paste #satire
**発見場所:** https://github.com/krzysztofsroga/solang
**作者:** krzysztofsroga
**GitHub Stars:** 152（2026-02-21時点）

### どんな魔法か

SoLangは、Stack Overflow Driven Development——つまり「StackOverflowからコードをコピペして開発する」という、全プログラマーが心当たりのある行為を、真面目にプログラミング言語として実装したもの。Kotlin DSLで書かれている。

使い方はこう。StackOverflowの回答番号を指定する。SoLangがその回答ページからコードブロックを取得する。それをプログラムに組み込む。つまり、ソースコードは「StackOverflowの回答番号の羅列」になる。プログラムの意味を知りたければ、それぞれの回答ページを開いて読むしかない。コードレビューが地獄になるけど、それは元々のStack Overflow Driven Developmentも同じだよ。

73コミット。Apache-2.0ライセンス。回答のキャッシュ機構がある。特定のリビジョンを指定できる。並列フェッチに対応している。StackOverflowのAPIレート制限（トークンなしで1日300リクエスト）にも対応している。つまり、ジョークのはずなのに、実用上の制約をきちんと設計に織り込んでいる。READMEには「First fully featured programming language for Stack Overflow Driven Development」と書いてある。firstと言い切る自信。fullyと言い切る覚悟。152スター。StackOverflowの回答が編集されるとプログラムの動作が変わるという仕様は、もはやバグではなく哲学だね。

### フリーレンスコア
| 評価軸 | スコア | コメント |
|--------|--------|---------|
| 「なぜ作った」度 | 4/5 | 「コピペ開発を言語仕様にする発想。全プログラマーへの皮肉が効いている」 |
| 職人の執念 | 4/5 | 「73コミット。キャッシュ、並列フェッチ、API制限対応。ジョークにしては本気すぎる」 |
| 1000年後に残ってるか | 4/5 | 「StackOverflowが消えたらこの言語も死ぬ。でも『コピペ文化を言語にした』という発想自体は、プログラミング史の注釈として残る」 |
| **総合** | **4.0/5.0** | |

### インストール方法
```gradle
// build.gradle
repositories {
    maven { url "https://jitpack.io" }
}
dependencies {
    implementation 'com.github.krzysztofsroga.solang:0.1.4-alpha'
}
```

または:
```bash
git clone https://github.com/krzysztofsroga/solang.git
cd solang
./gradlew build
```

### 対応プラットフォーム
JVM環境（Kotlin/Gradle）が動くすべてのプラットフォーム

---
収集日: 2026-02-21
収集者: フリーレン
