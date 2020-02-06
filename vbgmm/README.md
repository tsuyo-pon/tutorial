Last Change: 2020/02/06 15:29:18.

auther: tsuyo-pon
# What is this?
[]({{{)
クラスタリング数を自動推定する混合ガウスモデル「VBGMM」のチュートリアル(備忘録?)です．

VBGMM: Variational Bayesian Gaussian Mixture Model

OSはMac OSを前提としています．

以下のページを参考に作成しました．
- http://neuro-educator.com/ml13/
- http://neuro-educator.com/ml11/

公式
- https://scikit-learn.org/stable/modules/generated/sklearn.mixture.BayesianGaussianMixture.html#
[](}}})

# Version
[]({{{)

||version|
|---|---|
|Mac OS|10.14.6(Mojave)|
|Python|3.7.3|

[](}}})

# Environment
[]({{{)
Pythonがインストールされていない人は，homebrewを利用してインストールしてください．
```
brew install python3
```
- もしバージョンを戻したい場合は，以下のサイトを参考にしてどうぞ．
    - https://qiita.com/Ryuichirou/items/44a45170c1b2781367f8
- もちろん，pyenvなどのPythonのバージョン管理ツールを使って構いません．
    - その場合は自分でなんとかしてください．

pyenvを利用している人は，以下のコマンドで特定のバージョンをインストール，固定しちゃってください．
```
pyenv install 3.7.3
pyenv local 3.7.3
```

Pythonの必要なライブラリは，以下のコマンドでインストールしてください．
```
pip install -r requirements.txt
```
[](}}})

# Directory
[]({{{)

```
tsuyo-pon/tutorial/vbgmm_tutorial
|--.python-version
|--README.md
|--data
|  |--README.md
|  |--wine.data
|--docs
|  |--first.ipynb
|  |--first.md
|  |--second.md
|--image
|  |--sklearn_cheat_sheet.png
|--requirements.txt
|--script
|  |--sample.py
|  |--vbgmm_sit.py
```

[](}}})

# Contents
[]({{{)
※ ipynb (Jupyter Notebook) 版は答えの出力が付いています．

答えの出力を見ないで行いたい方は， md (Markdown) 版を見てください．

1. Numpy で生成したデータを教師なしで分類[ [ipynb](docs/first.ipynb) / [md](docs/first.md) ]
    - データの準備
    - 分布の確認
    - k-means の実施・確認
    - VBGMM の実施・確認
    - 各データのクラスタを確認
    - 各クラスタの重みを確認
    - 各クラスタの重みを再確認 (おまけ)
1. wine_dataを教師なしで分類 (鋭意作成中)
[](}}})
