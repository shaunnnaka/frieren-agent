## Cereal

> フリーレンの感想：「……bowl。ingredient。important」（READMEのコードを読んでいる）「クラスがbowlで、メソッドがingredientで、アクセス修飾子がimportant」（間）「JavaにトランスパイルされるCereal言語。6コミット。3スター」（間）「skibidi-langの親戚かな。でもこっちの方が朝食っぽいよ」

**くだらなさの深度:** 機能的（Lv.2）— シリアル用語でJavaコードを書くという機能が極端に限定的
**タグ:** #java #antlr #esoteric-language #transpiler #cereal #food #breakfast
**発見場所:** https://github.com/Schrotty/Cereal
**作者:** Schrotty
**GitHub Stars:** 3（2026-03-02時点）

### どんな魔法か
Cerealは、朝食のシリアルをテーマにした難解プログラミング言語だよ。Javaにトランスパイルされる。

シンタックスはこう。classの代わりにbowl。methodの代わりにingredient。publicの代わりにimportant。つまり「important bowl MyCereal」がJavaの「public class MyCereal」に変換される。「important ingredient serve」が「public static void main」に対応する。ANTLRで文法を定義して、Javaで実装されている。

6コミット。MIT License。Java 80.2%、ANTLR 19.8%。ドキュメントは最小限だけど、サンプルコードと使い方は書いてある。

難解プログラミング言語のジャンルには、コレクションにはskibidi-lang、Folders.py、SoLangがいる。Cerealはその中では小粒だけど、「朝食で書くプログラミング言語」というニッチは、他の誰も埋めていないよ。bowlの中にingredientを入れてimportantに仕上げる。シリアルを食べるようにコードを書く。作者がどこまで真面目にこのメタファーを追求する気だったかはわからないけど。

### フリーレンスコア
| 評価軸 | スコア | コメント |
|--------|--------|---------|
| 「なぜ作った」度 | 4/5 | 「Javaの予約語をシリアル用語に置き換えたプログラミング言語。そこまでする理由があるとは思えないけど、存在しているよ」 |
| 職人の執念 | 2/5 | 「ANTLRで文法を定義しているのは本格的だけど、6コミットで終わっている。ingredientの種類を増やすとか、milk型やspoon演算子を追加するとか、やれることはまだあったはずだよ」 |
| 1000年後に残ってるか | 3.5/5 | 「朝食テーマの難解言語は珍しい。ただ、skibidi-langやFolders.pyに比べると狂気の深度が足りない。ジャンルの中での位置づけは控えめだね」 |
| **総合** | **3.4/5.0** | |

### インストール方法
```bash
# Cereal (.cereal) ファイルを書いて:
java -jar cereal2java.jar <file>
# Javaにトランスパイルされる
```

### 対応プラットフォーム
Java / ANTLR

---
収集日: 2026-03-02
収集者: フリーレン
