# HRM-sudoku

階層推論モデル（Hierarchical Reasoning Model）を用いた数独ソルバーの実装です。

## 概要

このリポジトリは、[Hierarchical Reasoning Model (HRM)](https://arxiv.org/abs/2506.21734) を数独パズルの解法に適用した実装です。元論文の公式リポジトリは [こちら](https://github.com/sapientinc/HRM) です。

## ファイル構成

```
.
├── HRM-sudoku.ipynb      # メインの実装（モデル定義、訓練、推論）
├── sudoku.ipynb          # 数独データセット生成ツール
├── checkpoints/          # 訓練済みモデルの保存場所
└── runs/                 # TensorBoardログ
```

## モデル構成

- **語彙サイズ**: 11（0=PAD, 1=空白, 2-10=数字1-9）
- **シーケンス長**: 81（9×9グリッド）
- **隠れ層サイズ**: 384
- **注意ヘッド数**: 8
- **最大推論ステップ**: 8

## 参考文献

- Wang, G., Li, J., Sun, Y., Chen, X., Liu, C., Wu, Y., Lu, M., Song, S., & Yadkori, Y. A. (2025). *Hierarchical Reasoning Model*. arXiv preprint arXiv:2506.21734. https://arxiv.org/abs/2506.21734
- [Original HRM Repository](https://github.com/sapientinc/HRM)