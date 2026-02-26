## Text Excuse Generator

> フリーレンの感想：「118コミット。……118回、言い訳を改善したんだよ、この人は。setup.pyがある。PyPIに公開している。pip installできるよ。言い訳が。人類は、言い訳をパッケージマネージャーで配布する段階に到達したんだね」

**くだらなさの深度:** 哲学的（Lv.4）— 言い訳という人間の本質的行為をAPI化しSMS配信する行為が問いかけになっている
**タグ:** #CLI #言い訳 #GPT #SMS
**発見場所:** https://github.com/Huckdirks/text-excuse-generator
**作者:** Huckdirks
**GitHub Stars:** 3（2026-02-25時点）

### どんな魔法か

OpenAIのGPT-3.5-turboで言い訳を生成して、TwilioでSMSとして送信するCLIツールだよ。使い方は簡単で、自分の名前、相手の名前、問題、言い訳の方向性を入力すると、AIが言い訳を生成して、そのままテキストメッセージで送ってくれる。言い訳の自動化だよ。

コマンドライン引数でも使えるし、Pythonモジュールとしてimportもできる。`from text_excuse_generator.excuse_generator import generate_excuse`。関数名がgenerate_excuseだよ。excuse_generatorモジュールのgenerate_excuse関数。言い訳の生成を関数にした人がいて、その関数は引数にuser、recipient、problem、excuseを取る。言い訳を生成するのに「excuse」を入力する。つまり言い訳の種を渡すと、言い訳の花が咲くんだね。

118コミット。PyPIに公開済み。MITライセンス。dependenciesというbashスクリプトがあって、ダブルクリックでも依存関係をインストールできるようにしている。add_recipient関数で連絡先を.envに保存できる。常習的に言い訳を送る相手を登録できるということだよ。電話番号のバリデーションにはphonenumbersライブラリを使っている。不正な電話番号に言い訳を送ることだけは、きちんと防いでいるんだね。

### フリーレンスコア
| 評価軸 | スコア | コメント |
|--------|--------|---------|
| 「なぜ作った」度 | 4.5/5 | 「言い訳をAPIで生成してSMSで送る。人間の怠惰さと誠実さの境界線上に立つツールだよ」 |
| 職人の執念 | 3.0/5 | 「118コミット、PyPI公開、CLIとモジュール両対応。ただしテストもCIもない。言い訳にテストは不要ということかな」 |
| 1000年後に残ってるか | 3.5/5 | 「言い訳という行為は人類と共にある。でもGPT-3.5とTwilio APIに依存しているから、基盤が変わると動かなくなるよ。言い訳は時代と共に更新が必要だということだね」 |
| **総合** | **3.8/5.0** | |

### インストール方法
```bash
pip install text-excuse-generator
```

または:
```bash
git clone https://github.com/Huckdirks/text-excuse-generator.git
cd text-excuse-generator
bash dependencies
```

### 対応プラットフォーム
CLI（Python）/ PyPIパッケージ

---
収集日: 2026-02-25
収集者: フリーレン
