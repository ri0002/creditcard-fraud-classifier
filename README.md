# creditcard-fraud-classifier

クレジットカード不正検出のための機械学習モデル（RandomForest / ロジスティック回帰）

---

## 📘 背景（大学院課題）

本プロジェクトは、大学院講義『プログラミング基礎Ⅱ』の第8回課題として取り組んだものです。  
Kaggle上の [Fraud Detection Credit Card データセット](https://www.kaggle.com/datasets/yashpaloswal/fraud-detection-credit-card) を使用し、クレジットカード不正検出という社会課題の解決にチャレンジしました。

---

## 🔍 工夫した点

- **大規模データ（約28万件）のサンプリング**（20,000件に削減）
- **数値データ前提の標準化処理（StandardScaler）**
- **RandomForest + RandomizedSearchCV** によるハイパーパラメータ最適化
- **ロジスティック回帰との精度比較**
- **評価指標を網羅的に出力**（Accuracy / Precision / Recall / F1 / ROC AUC）
- **関数化と例外処理による保守性・再利用性の向上**

---

## 🧠 使用モデルと手法

| モデル                | 概要                                             |
|-----------------------|--------------------------------------------------|
| RandomForestClassifier | 決定木のアンサンブル、ランダムサーチでパラメータ最適化 |
| LogisticRegression     | ベースラインとして使用（高速・軽量）             |

使用ライブラリ：
- `scikit-learn`
- `pandas`
- `numpy`

---

## 📊 精度結果（Test Accuracy）

- **RandomForestClassifier**
  - **Test ROC AUC**: `0.9992`
  - 高い Precision / Recall / F1 も達成（詳細は出力参照）

- **LogisticRegression**
  - 精度はやや低いが、処理速度に優れるためベースライン比較に有効

※テストデータには全体の **40%** を使用（3割以上の条件を満たす）

---

## 🛠️ 実行方法（`.py` ファイル使用）

1. Kaggle から `creditcard.csv` をダウンロード  
   🔗 [データセットリンク](https://www.kaggle.com/datasets/yashpaloswal/fraud-detection-credit-card)
2. ファイルを `/content/creditcard.csv` に配置
3. Google Colab またはローカル環境で `main()` を実行（`creditcard-fraud-classifier.py`）

---

## 📁 データファイル（参考）

CSVファイルはサイズが大きいため、Google Drive にアップロードしています：

📂 [creditcard.csv（Google Drive）](https://drive.google.com/file/d/16jyD7s2UGb3gz-GHggTliP9Cyb3JCCyM/view?usp=drive_link)

---

## 👨‍🎓 提出概要（大学院）

> Kaggleの「Fraud Detection Credit Card」データを用いて、クレジットカード不正利用の検出モデルを構築。  
> サンプリング、前処理、ハイパーパラメータ最適化、再利用性の高い関数化に重点を置きました。  
> **Test ROC AUC は 0.9992**、また提出要件としてテストには全データの40%を使用しました。
