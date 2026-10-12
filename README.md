---
language:
- ja
license: grok2-community
pretty_name: 空手部語録データセット
configs:
- config_name: default
  data_files:
  - split: train
    path: data-karate.csv
tags:
- nlp
- dictionary
---

# 空手部（淫夢）語録データセット

真夏の夜の淫夢・空手部章に関連する語録・台詞・元ネタ情報をまとめたデータセットよ。

## 構成カラム

- `original_term`: 語録・台詞
- `japanese_reading`: 読み（ひらがな）
- `chinese_reading`: 中国語表記
- `english`: 英語表記
- `source_company` / `source_cuntory` / `source_series` / `source_season` / `source_chapter`: 出典・元ネタ情報
- `category`: 分類
- `said_by`: 発言者
- `background`: 解説・背景

## 使い方

```python
from datasets import load_dataset

dataset = load_dataset("z0uy1n/inmu")
print(dataset["train"][0])

```


---

### 2. 表示と動作を確認する

1. **Dataset Viewer の確認**
   `README.md` を保存後、データセットのトップページ（`Dataset card` タブ）に戻ると、数十秒でデータセットプレビューが自動生成されて、ブラウザ上でテーブル表示・検索ができるようになるわよ。

2. **Pythonからの読み込みテスト**
   手元の Python や Google Colab などで以下のコードを実行して、正常にロードできるか試してみてね。

   ```python
   from datasets import load_dataset

   # リポジトリから直接読み込み
   ds = load_dataset("z0uy1n/inmu")

   # 先頭データを確認
   print(ds["train"][0])

```

https://docs.google.com/spreadsheets/d/1uL-9M_Wf8kogJVS0Cb0PZosuuluI0REcoWupQpjbBVA/edit?usp=sharing