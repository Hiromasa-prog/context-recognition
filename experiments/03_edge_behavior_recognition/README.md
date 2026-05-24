# Edge Behavior Recognition

加速度センサデータを用いた軽量行動分類実験コード。

## Overview

本ディレクトリでは，
加速度センサデータを用いた軽量行動認識を行う．

エッジデバイス上での推論を想定し，
低計算量な分類手法を用いた行動分類を評価する．

また，
教師なしクラスタリングによって得られた状態系列を利用し，
クラスタベース行動認識の有効性を検証する．

本実験では，
教師なしクラスタリングによって抽出された状態情報を
行動認識へ利用することで，
ラベル依存を低減した軽量認識を目指す．

## Structure

```text
notebooks/
    01_edge_behavior_classification_pipeline.ipynb

experiments/
    binary_classification_strategy.ipynb
    multiclass_behavior_classification.ipynb
```

### notebooks/
軽量行動認識の基本パイプラインを実装する．

### experiments/
分類戦略や分類設定の比較実験を行う．
- binary_classification_strategy.ipynb
    - クラスごとの2値分類戦略を評価

- multiclass_behavior_classification.ipynb
    - 多クラス行動分類を評価

## Input

- 加速度特徴量
- クラスタリング結果
- 行動ラベル

## Output

- 行動分類結果
- 分類精度
- 推論評価結果

## Methods

- 軽量行動分類
- クラスタベース分類
- 2値分類戦略
- 多クラス分類