# Pytorchを用いた強化学習勉強
## 参考書籍
[作りながら学ぶ！深層強化学習]

## 目的, 目標
強化学習について学んできた知識を形にアウトプットする。
体系的な知識を身につける

## 環境
### pythonを用意
pyenvでanacondaをインストールし、ディレクトリにlocalで反映

`requirements.txt`に出力してるけどanacondaに任せたほうがいい
anaconda3-5.0.0を何らかの手段で用意して

```
conda install keras
```
で互換ライブラリもいい感じにアップデートしてくれるのでいい感じになる

### openAI gym環境構築

pipとcondaでgym本体と動画生成に必要なモジュールを入れる
pipとcondaを一緒に使うのは芳しくないけどpyenvなりconda envなりで作った使い捨て環境なので何も問題はない。

```
pip install gym && pip install JSAnimation
```

```
conda install -c conda-forge ffmpeg
```

pygletは1.2.4じゃないとgymのjupyternotebookでの描写がエラーを吐くんだけど
conda installで引っ張られるので最後にversion指定してインストールしてあげる

```
pip uninstall pyglet -y && pip install pyglet==1.2.4
```
### macの環境も整える
```
brew install cmake boost boost-python sdl2 swig wget
```

もうちょっとスマートにまともなやり方もあるけど面倒くさいしとりあえず現状問題ないのでこれで
なにか問題発生したら調整します


## 余談
docker-composeで構築するのもありだから気が向いたらそっちに映るかも

あとはjupyter notebookのプラギン設定をどっかにまとめたい
