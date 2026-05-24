# Context Recognition Research

## 概要

本リポジトリは，加速度センサとビーコン信号を用いたマルチモーダルコンテキスト認識の研究パイプラインをまとめたものである．

本研究では以下を目的としている：

- センサ時系列データから潜在的な行動状態を抽出する
- クラスタリングを用いて手動ラベル付けコストを削減する
- エッジデバイス上で動作可能な軽量行動認識を実現する
- 位置情報と動作情報を統合し，コンテキスト理解を行う

主に以下の要素を扱う：

- 加速度センサ
- ビーコン位置推定
- 教師なしクラスタリング
- 軽量行動認識
- マルチモーダル統合

---

# 研究パイプライン

## 動作認識パイプライン

```text
Raw Acceleration Data
        ↓
Preprocessing
        ↓
Feature Engineering
        ↓
Unsupervised Clustering
        ↓
Lightweight Behavior Recognition
```

## 位置推定パイプライン

```text
Beacon RSSI Signals
        ↓
Beacon Localization
        ↓
Location Estimation
```

## 最終統合

```text
Behavior Recognition + Localization
                ↓
        Context Recognition
```

---

# Repository Structure

```text
context-recognition/
├── paper/
├── slides/
└── experiments/
    ├── 01_preprocessing/
    ├── 02_clustering/
    ├── 03_edge_behavior_recognition/
    └── 04_beacon_localization/
```

---

# 実行順序

```text
01_preprocessing
        ↓
02_clustering
        ↓
03_edge_behavior_recognition

04_beacon_localization
        ↓

Behavior Recognition + Localization
        ↓
Context Recognition
```