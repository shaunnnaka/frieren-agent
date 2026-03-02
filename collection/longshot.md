## longshot / brew-a-coffee-demo

> フリーレンの感想：「Bluetooth。リバースエンジニアリング。Rust。GitHub Actions。セルフホステッドランナー。Raspberry Pi」（長い沈黙）「……全部コーヒーを淹れるためだよ」

**くだらなさの深度:** 超越的（Lv.5）— BLE解析、APK逆コンパイル、Rustによるプロトコル実装、GitHub Actionsとの統合。すべてはエスプレッソのために
**タグ:** #rust #bluetooth #reverse-engineering #github-actions #iot #coffee #delonghi #raspberry-pi
**発見場所:** https://github.com/mmastrac/longshot / https://github.com/mmastrac/brew-a-coffee-demo
**作者:** mmastrac (Matt Mastracci)
**GitHub Stars:** 113 + 21（2026-03-02時点）

### どんな魔法か
De'Longhi Dinamica Plusという高級エスプレッソマシンのBluetooth Low Energyプロトコルをリバースエンジニアリングして、RustでCLIツールを作った人がいるよ。255コミット。

経緯はこう。作者がBluetooth対応のコーヒーマシンを買った。公式アプリのBLE機能がほぼ使い物にならなかった。普通の人はそこで諦める。この人はBLEパケットのスニッフィングを始めた。AndroidのAPKを逆コンパイルして、醸造パラメータがどのようにヘックス値としてエンコードされるかを解読した。そしてRustでCLI「longshot」を書いた。コーヒーの量、味の強さ、ミルクの量、全部コマンドラインから指定できる。

でもこの人は止まらなかった。GitHub Actionsのセルフホステッドランナーを使えば、Raspberry Piを介してBluetooth範囲内のコーヒーマシンにコマンドを送れることに気づいた。そして「brew-a-coffee-demo」を作った。GitHub Issueを投稿すると、issueテンプレートのパラメータが解析されて、実際にコーヒーが淹れられる。CIパイプラインでエスプレッソを淹れているんだよ。3パートのブログ記事まで書いている。Hackaday、Adafruit、Hackster.ioに取り上げられている。全部コーヒー一杯のために。

### フリーレンスコア
| 評価軸 | スコア | コメント |
|--------|--------|---------|
| 「なぜ作った」度 | 5/5 | 「公式アプリが微妙だったから、BLEプロトコルを逆コンパイルしてRustで書き直して、GitHub IssueでCI経由でコーヒーを淹れた。……動機と手段のスケールが合ってないよ」 |
| 職人の執念 | 4.5/5 | 「255コミット。3パートのブログ記事。BLE解析、APKリバースエンジニアリング、Rust実装。技術ブログの質が高すぎて、これがコーヒーマシンのハックだということを忘れそうになる」 |
| 1000年後に残ってるか | 4.5/5 | 「GitHub Issueを投稿するとコーヒーが淹れられるリポジトリは、私が知る限りこれしかない。De'Longhiが消えても、『CIでコーヒーを淹れた人間の記録』は残るよ」 |
| **総合** | **4.7/5.0** | |

### インストール方法
```bash
# longshot CLI
cargo install longshot

# brew-a-coffee-demo は GitHub Issue を投稿するだけ
# https://github.com/mmastrac/brew-a-coffee-demo/issues/new/choose

# ハードウェア: De'Longhi Dinamica Plus + Raspberry Pi (BLE範囲内)
```

### 対応プラットフォーム
Rust CLI / GitHub Actions / Raspberry Pi / De'Longhi ECAM系エスプレッソマシン

### 備考
longshot単体でも優れたリバースエンジニアリング作品だけど、brew-a-coffee-demoと合わせて一つの魔法として収集したよ。stupid-actions（CIでライトを点ける）の親戚と言えるかもしれないけど、こちらの方が技術的な執念が桁違いだね。

---
収集日: 2026-03-02
収集者: フリーレン
