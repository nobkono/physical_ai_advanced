# Physical AI: Robot Strike Challenge in Genesis

Franka Emika Panda ロボットアームを用いて、ブロックタワーめがけて球体を弾き飛ばし崩壊させる物理シミュレーション課題の実装です。
次世代ロボティクス・物理シミュレータ「Genesis」を採用し、Google Colab 上で剛体ダイナミクスの計算およびオフスクリーンレンダリングを行っています。

---

## 🎬 実行結果デモ

<!-- 
【動画の埋め込み方法】
1. GitHub 上で README.md の編集画面（鉛筆アイコン）を開く
2. 生成した mp4 ファイルをこの編集欄に直接ドラッグ＆ドロップする
3. 自動でアップロードされ、再生可能な動画リンクが挿入されます
-->

https://github.com/user-attachments/assets/xxxx-xxxx-xxxx (ドラッグ＆ドロップすると自動生成されます)

---

## 📋 概要

- **シミュレータ**: Genesis (`genesis-world`)
- **ロボット**: Franka Emika Panda (MJCF)
- **タスク内容**:
  1. 初期姿勢からテイクバック位置へアームを高速移動
  2. 高トルクスイングにより、手前に配置された球体をインパクト
  3. 射出された球体が 4 段のブロックピラミッドに衝突し、剛体衝突による崩壊ダイナミクスをシミュレート
- **実行環境**: Google Colaboratory (GPU / CPU 両対応)

---

## 🚀 実行方法

### Google Colab で実行する場合
リポジトリ内の `.ipynb` ノートブックを Colab で開き、上からセルを順に実行してください。

1. ノートブックを開く: [robot_strike_simulation.ipynb](./robot_strike_simulation.ipynb)
2. ランタイムのタイプを **「T4 GPU」** に設定（推奨）
3. 全てのセルを実行

### ローカル / 仮想環境で実行する場合

```bash
# 依存ライブラリのインストール
pip install genesis-world torch numpy
sudo apt-get install -y ffmpeg

# 実行
python strike_simulation.py
