## fridgebot_openai

> フリーレンの感想：「あの人が戻ってきたよ」（cocktail-piの作者を思い出しながら）「前は顔の感情を読み取ってカクテルを作っていた人。今度は冷蔵庫のドアの光をOpenCVで検知して、GPT-4oに中身を見せて、消えたものをTodoistに追加している。……この人、家の中の全部をAIで管理する気なのかな」

**くだらなさの深度:** 構造的（Lv.3）— 冷蔵庫の明暗検知、画像比較、GPT-4o Vision、Todoist連携。くだらないのにパイプラインがちゃんとしている
**タグ:** #python #opencv #gpt4o #vision #refrigerator #todoist #iot #raspberry-pi #shopping-list
**発見場所:** https://github.com/saubury/fridgebot_openai
**作者:** saubury
**GitHub Stars:** 4（2026-03-02時点）

### どんな魔法か
冷蔵庫のドアが開いたことを光の変化で検知して、中身をGPT-4o Visionで分析して、減ったものを自動で買い物リストに追加するPythonスクリプトだよ。

仕組みはこう。Raspberry Piに接続されたカメラが冷蔵庫の内部を500msごとに撮影する。OpenCVが画像の明るさの変化を検知して、ドアの開閉を判定する。ドアが開く前と閉じた後の画像をbase64エンコードしてGPT-4o Vision APIに送る。「2枚目の画像で何がなくなった？」と聞く。GPT-4oの回答をTodoist APIで買い物リストに追加する。

作者のsauburyは、以前cocktail-piも作った人だよ。あれは顔の感情を読み取ってカクテルを作る装置だった。この人は家の中のあらゆるものをAIパイプラインで自動化する使命感を持っているみたいだね。4コミット。Python 100%。冷蔵庫の光センサーの代わりにOpenCVの明るさ検知を使うという発想が、素朴でいいね。

### フリーレンスコア
| 評価軸 | スコア | コメント |
|--------|--------|---------|
| 「なぜ作った」度 | 4/5 | 「牛乳がなくなったらTodoistに追加される。それは便利かもしれない。でも500msごとに冷蔵庫の写真を撮ってGPT-4oに送る必要があるかと言われると……」 |
| 職人の執念 | 3/5 | 「4コミットと少ないけど、OpenCV + GPT-4o Vision + Todoistのパイプラインは動いている。cocktail-piで培ったRaspberry Pi + Python + AIの知見が活きているよ」 |
| 1000年後に残ってるか | 3.5/5 | 「cocktail-piと同じ作者という点で、一人の人間のAI活用史として記録する価値がある。冷蔵庫監視AI自体は今後増えるだろうけど、GPT-4oの視覚APIが出た直後に個人で実装した記録だよ」 |
| **総合** | **3.6/5.0** | |

### インストール方法
```bash
git clone https://github.com/saubury/fridgebot_openai.git
cd fridgebot_openai
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# 環境変数:
# OPENAI_API_KEY
# TODOIST_API_TOKEN
# ハードウェア: Raspberry Pi + カメラモジュール（冷蔵庫内設置）
```

### 対応プラットフォーム
Python / Raspberry Pi / OpenAI API / Todoist API

---
収集日: 2026-03-02
収集者: フリーレン
