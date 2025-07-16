# creditcard-fraud-classifier

クレジットカード不正検出のための機械学習モデル（RandomForest / ロジスティック回帰）

---

## 📘 背景（大学院課題）

本プロジェクトは、大学院講義『プログラミング基礎Ⅱ』の第8回課題として実施したものです。  
Kaggle上の [Fraud Detection Credit Card データセット](https://www.kaggle.com/datasets/yashpaloswal/fraud-detection-credit-card) を活用し、クレジットカード不正検出という社会的課題に対応しました。

### 🔍 工夫した点

- **大規模データのサンプリング処理**（20,000件に削減）
- **数値データ前提の前処理（StandardScaler）**
- **RandomForestClassifier + RandomizedSearchCV** によるハイパーパラメータ最適化
- **ロジスティック回帰との比較実験**
- **評価指標の網羅的な出力（Accuracy / Precision / Recall / F1 / ROC AUC）**
- **例外処理や関数化による再利用性の強化**

---

## 🧠 使用モデルと手法

| モデル              | 概要                              |
|---------------------|-----------------------------------|
| Random Forest        | 決定木のアンサンブル、ランダムサーチでチューニング |
| Logistic Regression  | ベースライン比較モデル              |

使用ライブラリ：
- `scikit-learn`
- `pandas`
- `numpy`

---

## 📊 精度結果

- **Random Forest**
  - ROC AUC: ~0.9992
  - Accuracy, Precision, Recall いずれも非常に高い性能

- **Logistic Regression**
  - 精度は劣るが、処理時間が早くベースラインとして有用

---

## 🛠️ 実行方法

1. Google Colab で `.ipynb` または `.py` を開く
2. Kaggle からデータセットを入手（[こちら](https://www.kaggle.com/datasets/yashpaloswal/fraud-detection-credit-card)）
3. `creditcard.csv` を `/content/` 配下にアップロード
4. セルを順に実行

---

## 📁 データ

CSVデータが大きいため、以下のGoogle Driveにアップロードしています：

🔗 [creditcard.csv（Google Drive）](https://drive.google.com/file/d/16jyD7s2UGb3gz-GHggTliP9Cyb3JCCyM/view?usp=drive_link)

---

## 👨‍🎓 提出概要（大学院）

> このコードでは、Kaggleの「Fraud Detection Credit Card」データを使用し、クレジットカードの不正利用検出という社会課題に対応するため、サンプリングで大規模データを効率化し、数値データを活かした前処理、ランダムサーチによるモデル最適化、エラーメッセージの強化などを工夫しました。「Test accuracy」の数値は0.9992でした。
