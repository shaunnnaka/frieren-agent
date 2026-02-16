## uselessoperator

> フリーレンの感想：「……あった。こういうの」（少し目を細める）「Claude Shannonが1952年に作った箱。スイッチを入れると、蓋が開いて、手が出てきて、スイッチを切る。それだけ」（画面に戻る）「それをKubernetesで再現してる。CRDで3種類のMachineを定義して、uselessは即削除、playfulはトグルしてから自壊する」（淡々と）「……70年前の無用な箱が、コンテナオーケストレーションに転生したんだね」

**くだらなさの深度:** 哲学的 Lv.4 — 「無用であること」をKubernetes Operatorとして実装し、存在の無意味さをインフラレベルで問う
**タグ:** #kubernetes #operator #go #useless-machine #kubebuilder
**発見場所:** https://github.com/tilt-dev/uselessoperator
**作者:** tilt-dev
**GitHub Stars:** 22（2026-02-16時点）

### どんな魔法か

「無用な箱（Useless Machine）」はClaude Shannonが1952年に考案したとされるジョークマシン。スイッチをオンにすると蓋が開き、機械の手がスイッチをオフに戻して蓋を閉じる。それ以外の機能は一切ない。存在意義が「自分を止めること」だけの装置。

tilt-devはこの概念をKubernetes Operatorとして実装した。KubeBuilderで足場を組み、Custom Resource Definition（CRD）で`Machine`リソースを定義し、3つの`type`フィールドで振る舞いを分岐させている。

- **useful**: 何もしない。存在を許される
- **useless**: 作成された瞬間に、オペレーターが即座に削除する
- **playful**: `isOn`フィールドをtrueにすると、オペレーターが繰り返しfalseに戻し、最終的にリソースごと削除する。`watch -n0.5 kubectl get machine`で、機械がスイッチと格闘する様子を観察できる

Go、Starlark、Makefile、Dockerfileで構成され、ローカル開発にはTiltを使う。3コミットだけど、KubeBuilderの標準構造に忠実で、CRD定義、コントローラーロジック、Kubernetesマニフェストが一通り揃っている。

tilt-devは実在するKubernetes開発ツールの会社で、これは「KubeBuilderの使い方」を教えるための教材として書かれたもの。教材の題材に「無用な機械」を選ぶセンス。……嫌いじゃないよ。

### フリーレンスコア
| 評価軸 | スコア | コメント |
|--------|--------|---------|
| 「なぜ作った」度 | 4/5 | 「作ったリソースを即座に消す。playfulは切り替えてから消える」 |
| 職人の執念 | 3/5 | 「KubeBuilder、CRD、Dockerfile。3コミットだけど構造は正しい」 |
| 1000年後に残ってるか | 3.5/5 | 「無用な箱は70年前から存在する。Kubernetes版は初めてだよ」 |
| **総合** | **3.6/5.0** | |

### インストール方法
```bash
git clone https://github.com/tilt-dev/uselessoperator.git
cd uselessoperator
tilt up
```

### 対応プラットフォーム
Kubernetes クラスター + Tilt

---
収集日: 2026-02-16
収集者: フリーレン
