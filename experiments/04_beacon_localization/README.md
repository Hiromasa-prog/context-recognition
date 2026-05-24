# Beacon Localization

ビーコンデータを用いた位置推定・位置分類実験コード。

## Overview

ビーコンRSSIデータを利用し，
作業者位置の推定および位置状態分類を行う．

また，
複数中継器から取得したRSSI情報を用いて，
位置推定に有効な特徴量設計を評価する．

本位置推定結果は，
最終的に行動認識結果と統合し，
コンテキスト認識へ利用される．

## Structure

```text
notebooks/
    01_beacon_localization_pipeline.ipynb

experiments/
    unsupervised_feature_experiment.ipynb
```

### notebooks/
ビーコン位置推定の基本パイプラインを実装する．

### experiments/
特徴量設計および教師なし特徴利用の比較実験を行う．
- unsupervised_feature_experiment.ipynb
    - 教師なし特徴量を用いた位置分類性能を評価

## Input

- ビーコンRSSIデータ
- 中継器情報

## Output

- 推定位置
- 位置分類結果
- 特徴量データ