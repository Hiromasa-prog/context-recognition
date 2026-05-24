# Unsupervised Behavior Clustering

加速度センサデータを用いた行為クラスタリング実験コード。

## Overview

本ディレクトリでは，
加速度センサ時系列データに対して教師なしクラスタリングを適用し，
潜在的な行動状態の抽出を行う．

主に TICC を用いた時系列クラスタリングを実施し，
クラスタ結果を行動認識へ利用する．

また，以下の比較実験を行う：

- k-meansとの比較
- window size変更時の挙動比較
- クラスタベース分類性能評価

本クラスタリング結果は後段の軽量行動認識で利用される．

## Structure

- notebooks/
  - TICCクラスタリング
  - クラスタ解析
  - 状態遷移可視化

- experiments/
  - k-means比較実験
  - window size比較
  - 分類性能比較

## Methods

- TICC
- k-means
- 時系列特徴量抽出
- windowベース時系列分割
- クラスタラベル写像

## Data

入力:
- 加速度センサデータ

## Input

- 前処理済み加速度データ
- 特徴量データ

## Output

- クラスタラベル
- 行動状態系列
- クラスタ可視化結果
- 分類用特徴量

## Environment

Python

主要ライブラリ:
- numpy
- pandas
- scikit-learn

## Notes

TICCライブラリは別途導入が必要。