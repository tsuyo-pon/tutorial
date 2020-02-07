Last Change: 2020/02/07 13:10:44.

auther: tsuyo-pon
# What is this?
[]({{{)
### Sound Signal Processing

音響解析の基礎技術についての解説です．

OSはMac OSを前提としています．

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

# Contents
1. [FFT](docs/fft.ipynb)
    - **サイン波の生成(Make a sine wave)**
    - **サイン波の合成(Make a synthesized sine wave)**
    - **高速フーリエ変換(Fast Fourier Transform)**
    - **短時間フーリエ変換(Short-time Fourier Transform)**
1. [IFFT](docs/ifft.ipynb)
    - サイン波の生成(Make a sine wave)
    - サイン波の合成(Make a synthesized sine wave)
    - 高速フーリエ変換(Fast Fourier transform)
    - **逆フーリエ変換(Inverse Fourier Transform)**
1. [Bandpass](docs/bandpass.ipynb)
    - サイン波の生成(Make a sine wave)
    - サイン波の合成(Make a synthesized sine wave)
    - **低域通過フィルタ(Low pass filter)**
    - **高域通過フィルタ(High pass filter)**
    - **帯域通過フィルタ(Band pass filter)**
    - **合成したサイン波の音声再生(Play a synthesized sine wave)**
    - **変換したサイン波の音声再生(Play a converted sine wave)**
    - **補足-音声の読み込み(read wav)**
