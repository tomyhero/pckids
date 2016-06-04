---
layout: default
---

# 宝探しゲームとは

ディレクトリとファイルを複数作成し、「あたり」と書かれたファイルを見つけるゲームです。


# インストール

## ダウンロード

gitをつかってとってきます。

```

cd ~/Desktop
git clone https://github.com/tomyhero/takarasagashi.git

```


## コンパイル

ソースコードから、ソフトを作ります。

```

cd takarasagashi
go build -o takarasagashi app.go

```

takarasagashi ファイルができましたか？


# 遊んでみる

## ゲームデータを作りましょう

以下を実行してみましょう。 「takara」というディレクトリができるはずです。

```

./takarasagashi

```

「あたり」をみつけましょう！


# ゲームデーターをカスタマイズする

## helpをみる

helpでなにができるか、聞いてみましょう。

```
./takarasagashi --help
```

このような表示がされましたか？

```
Usage of ./takarasagashi:
    -dir_count int
ディレクトリ数 (default 10)
    -file_count int
ファイル数 (default 20)
    -root_name string
    宝物のディレクトリ名 (default "takara")
```

ディレクトリ数の指定、ファイル数の指定、宝物のディレクトリ名の変更ができるみたいです。

## ディレクトリ数を変更してみる

ディレクリ数を１にしてゲームを簡単にしてみましょう。
前につくった、「takara」のディレクトリはごみばこにいれておきましょう。

```
./takarasagashi -dir_count 1
```

「takara」の中にディレクトリが一つだけしかつくられなかったかな？


## ファイル数も変更してみる

もっと簡単にしてみましょう。
前につくった、「takara」のディレクトリはごみばこにいれておきましょう。


```
./takarasagashi -dir_count 1 -file_count 2
```

２個しかファイルができなかったかな？


## ディレクトリ名も変更してみよう

```
./takarasagashi -root_name otakara
```

## いろいろ組み合わせてみよう

```
./takarasagashi -root_name takara01 -dir_count 10 -file_count 10
./takarasagashi -root_name takara02 -file_count 10

```

## tree コマンドでみてみよう

```

cd takara
tree

```

treeコマンドが入ってない場合は、インストールしておこう。

```

brew install tree

```

# 改造してみよう（応用）

takarasagashiゲームは、go言語でできています。
改造してみよう。


## 作成するディレクトリをふやしてみよう

app.go　を vimでひらいてみよう。ディレクトリ名を設定している、配列があります。
自由に、追加してみよう。

```

cd ~/Desktop/takarasagashi
vim app.go

```

```

var DIR_NAMES []string = []string{"isu", "tukue", "hako", "kokuban", "kuruma", "densya", "sora"}

```

改造したら、buildしよう

```

go build -o takarasagashi app.go

```

## もっといろいろ改造してみよう

* ファイル名を追加したり
* 「はずれ」を「ざんねんでした」にしたり

それいがいにも、自分で考えておもしろく改造してみよう！



