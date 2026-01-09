# 生産管理中間レポート

本リポジトリは、生産管理のためのSKABデータセットを用いたモデル比較分析およびレポート作成を目的としています。

---

## プロジェクト構成

```
.
├── data
│   ├── treated-data/            # 前処理済みデータ
│   └── unprocessed-data/        # 取得した生データ
├── docs/
│   └── 生産管理_中間課題.docx      # 提出レポート
├── models/
│   ├── xgb_gbm_YYYYMMDD_HHMMSS.pkl # 保存済モデル
├── notebook/
│   ├── 1-01-get-data.ipynb         # データ収集
│   ├── 1-02-data-engineering.ipynb # データ前処理
│   ├── 1-03-construct-xgb-model.ipynb # XGBoostモデル構築
│   └── 1-04-model-tuning.ipynb     # モデルチューニング
├── requirements.txt                # 必要なPythonパッケージ
├── README.md                       # 本ファイル
```

---

## 使い方

### 1. データ取得

データセットの取得は、`notebook/1-01-get-data.ipynb`を実行してください。  
`data/unprocessed-data/`に生データが格納されます。

### 2. データ前処理

下記ノートブックで前処理を行います。

- `notebook/1-02-data-engineering.ipynb`

前処理後のデータは`data/treated-data/`に保存されます。

### 3. モデル構築・チューニング

- `notebook/1-03-construct-xgb-model.ipynb`  
  XGBoostによるモデルの学習
- `notebook/1-04-model-tuning.ipynb`  
  ハイパーパラメータ調整

学習済みモデルは`models/`配下に出力されます。

---

## ファイル説明

- `data/`: データセット格納先
  - `treated-data/`: 前処理後データ
  - `unprocessed-data/`: 取得した生データ
- `docs/`: ドキュメント・レポート
- `models/`: 学習済みモデルファイル
- `notebook/`: 分析用Jupyter Notebook
- `requirements.txt`: 必要なPythonパッケージ一覧
- `README.md`: プロジェクト説明ファイル

---

## 環境構築

必要なライブラリは、下記コマンドでインストールできます：

```sh
pip install -r requirements.txt
```

---

## 備考

- レポート提出用ファイルは`docs/`に格納しています。
- モデル名には学習日時(YYYYMMDD_HHMMSS)が付与されます。
