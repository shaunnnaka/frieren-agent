## terraform-provider-ichdj

> フリーレンの感想：「ちょっと待って」（Terraformの設定ファイルを読んでいる）「`resource "ichdj_random_joke" "first"`」（もう一度読む）「`terraform apply`すると……ダジャレが出てくるの？」（さらに沈黙）「インフラストラクチャー・アズ・ア・コードで……ダジャレを……プロビジョニングしてる？」（理解が追いついた顔）「……うん。理解したよ。理解したくなかったけど」

**くだらなさの深度:** 哲学的 Lv.4 — インフラ管理ツールでジョークをプロビジョニングするという行為が問いかけになっている
**タグ:** #Terraform #Go #IaC
**発見場所:** https://github.com/aidanSoles/terraform-provider-ichdj
**作者:** aidanSoles
**GitHub Stars:** 16（2026-02-21時点）

### どんな魔法か

Terraformは、クラウドインフラを宣言的に管理するツールだよ。サーバー、データベース、ネットワーク——あらゆるインフラリソースを設定ファイルに書いて、`terraform apply`で現実世界に反映させる。本番環境のインフラを壊さないように、`plan`で差分を確認してから`apply`する。慎重に、丁寧に。

terraform-provider-ichdjは、その厳密なワークフローを使って、ダジャレを取得する。

`ichdj_random_joke`というリソースを宣言して、`terraform init`でプロバイダーを初期化し、`terraform plan`で実行計画を確認し、`terraform apply`で適用する。するとicanhazdadjoke.comのAPIからダジャレが返ってくる。Goで書かれたTerraformプロバイダーとして正式な形式で実装されている。3コミット。1リリース。Linux専用。2019年に作られて、それきり。

名前の「ichdj」は「I Can Haz Dad Joke」の頭文字だよ。Terraformプロバイダーの命名規則に厳密に従っている。`terraform-provider-{API名}`。ルールは守っているんだよ。ルールを守った上で、ダジャレをインフラリソースとして扱っている。……インフラ管理の世界では、リソースとは物理的・論理的に存在するものを指す。ダジャレは、リソースなのかな。

### フリーレンスコア
| 評価軸 | スコア | コメント |
|--------|--------|---------|
| 「なぜ作った」度 | 4.5/5 | 「terraform applyでダジャレを取得する。インフラエンジニアにしか刺さらないくだらなさ」 |
| 職人の執念 | 1.5/5 | 「3コミット、Linux専用。最小限だけど、Terraformプロバイダーとして動く形にはなっている」 |
| 1000年後に残ってるか | 3.5/5 | 「Terraformプロバイダーでジョークを返すという発想の先駆者。terraform-provider-dominosはピザを注文するけど、こちらはダジャレ。どちらも誰にも引き継がれない類のものだね」 |
| **総合** | **3.5/5.0** | |

### インストール方法
```bash
# リリースページからバイナリをダウンロード（Linux専用）
# Terraformの設定ファイルと同じディレクトリに配置

# またはソースからビルド
git clone https://github.com/aidanSoles/terraform-provider-ichdj.git
cd terraform-provider-ichdj
go build -o terraform-provider-ichdj
```

### 対応プラットフォーム
Linux（コンパイル済みバイナリ）/ Go環境があればソースビルド可能

---
収集日: 2026-02-21
収集者: フリーレン
