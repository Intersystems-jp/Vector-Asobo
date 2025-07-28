
ウェビナー『ベクトルであそぼう!』 のソースコードです。

## 必要環境

- InterSystems IRIS (2024.3 以降, Community Edition / Advanced Server)
- Python 3.x（venv 推奨）
- Jupyter Notebook


### 1. IRIS (Community Edition)


InterSystems IRIS (2024.3 以降のCommunity Edition もしくは Advanced Server が必要です。)

IRIS Community Edition のダウンロード/インストールは下記をご覧ください。

 [InterSystems IRIS／InterSystems IRIS for Health コミュニティエディションのダウンロード方法](https://jp.community.intersystems.com/post/intersystems-iris%EF%BC%8Fintersystems-iris-health-%E3%82%B3%E3%83%9F%E3%83%A5%E3%83%8B%E3%83%86%E3%82%A3%E3%82%A8%E3%83%87%E3%82%A3%E3%82%B7%E3%83%A7%E3%83%B3%E3%81%AE%E3%83%80%E3%82%A6%E3%83%B3%E3%83%AD%E3%83%BC%E3%83%89%E6%96%B9%E6%B3%95)


### 2. Python 環境

### Python のインストールについて

本プロジェクトは **Python 3.x** が必要です。

- Windows の方は：[Python公式サイト](https://www.python.org/downloads/windows/) からダウンロードしてください。
- macOS の方は Homebrew を使ってインストールできます：

```bash
brew install python
```

### venv

Python の仮想環境（`venv`）を使うことで、依存関係や環境構築をプロジェクトごとに独立することができ、管理が簡単になります。

```bash

# 任意の名前(ここではfishenv)で環境を作成する
python -m venv fishenv

# 仮想環境を有効化する
fishenv\Scripts\activate     # Windows の場合
source fishenv/bin/activate  # macOS/Linux の場合

# PIPで必要なライブラリをインストールする
# (Jupyter Notebook の欄を参照ください)

# (参考)仮想環境を終了するには
deactivate
```

### 3. Jupyter Notebook
Jupyter Notebook のインストール

```bash
pip install jupyter
```

## 起動方法

* IRIS を起動します。
```bash
iris start (インスタンス名)
# もしくは、システムトレイから起動(Windowsの場合)
```

* 仮想環境を有効化します。

```bash
# 仮想環境を有効化する
fishenv\Scripts\activate     # Windows の場合
source fishenv/bin/activate  # macOS/Linux の場合

```
* notebook/iris_config.py を編集しIRISへの接続情報を記載してください。

* Jupyter Notebook を起動します。

```bash
jupyter notebook
```

* /notebook/配下のファイルをJupyter Notebook上で開きます
  * Prep.ipynb, FishNameAsobo.ipynb, VisualizeVector.ipynb を実行して実験を行ってください。
  * 実験完了後、データやテーブルが不要でしたら CleanUp.ipynbを実行してください。

## ソースコード

* notebook/iris_config.py
  * IRISへの接続情報を設定

* notebook/Prep.ipynb
  * テーブルの作成、データの登録

* notebook/FishNameAsobo.ipynb
  * 魚の写真から魚の名前をあてる実験

* notebook/VisualizeVector.ipynb
  * ベクトルの可視化 / クラスタリング / アノマリ検知

* notebook/CleanUp.ipynb
  * データの削除、テーブルの削除

## データセット

* datasets/fishname.csv
  *  魚の名前リスト

* datasets/super
  * スーパーで購入した魚の画像

* datasets/Wikipedia/image/
  * Wikipediaから取得した画像

* datasets/Wikipedia/CREDITS.md
  * ライセンス表記

