# 生産管理中間レポート

## 課題1: SKABデータを用いたモデル比較分析

### データの収集

データの収集は`notebook/1-1-get-data.ipynb`を用いて収集し`data/`に格納します。当該ファイルを実行してください。

### ディレクトリ構成

```bash
.
├── data
│   ├── treated-data                        # 加工後のデータ
│   └── unprocessed-data                    # 加工前(取得後)の生データ
├── docs
│   ├── ~$管理_中間課題.docx
│   └── 生産管理_中間課題.docx                  # レポート
├── models
│   ├── xgb_gbm_20251201_162850.pkl         # モデル名
│   └── xgb_gbm_20251201_162903.pkl
├── notebook
│   ├── 1-01-get-data.ipynb                 # (タスク)-(章)-(実行内容).ipynb
│   ├── 1-02-data-engineering.ipynb
│   ├── 1-03-construct-xgb-model.ipynb
│   └── 1-04-model-tuning.ipynb
├── README.md
└── requirements.txt
```