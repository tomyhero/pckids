---
layout: default
---

# hello Vim

## 概要

Vimを活用し、ファイルの作成、書き込み、保存を習います。


## Vim勉強用のディレクトリ作成


デスクトップ上に、vim ディレクトリを作ります。
その中で作業していきましょう。

```
mkdir  ~/Desktop/vim
cd ~/Desktop/vim
pwd
```


## ファイルオープン

ファイルをオープンしてみましょう。

```
vim hello.txt
```

## Insertモードにしてみましょう

Vimには、ノーマルモードとInsertモードというのがあります。
もじを書いたりするには、Insertモードにする必要がります。 ```i ``` とタイプしてみましょう。

画面の一番下に```-- INSERT --```と表示されましたか？表示されていれば、Insertモードになっています。


## Hello Vimとかいてみよう

Insertモードの時は、文字をかきこむことができます。

```Hello Vim```

と書いてみましょう。

## ノーマルモードに戻そう

```esc```キーを押すと、ノーマルモードに戻ります。```--INSERT--``` の表示がなくなっていれば、ノーマルモードです

## 保存してみよう

ノーマルモードで、 ```:w``` とタイプすると、保存されます。


## quitしてみよう


ノーマルモードで、 ```:q``` とタイプすると、ファイルを閉じることができます。

## もう一度開いてみよう


``` ls ```コマンドで、ファイルが存在するか調べてみよう。

ありましたか？では、もう一度ファイルを開いてみよう。

```
vim hello.txt
```

ひらけましたか？　前に書いた情報が残ってますね？ ``` :wq ``` でセーブして閉じましょう。
