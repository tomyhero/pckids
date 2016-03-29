---
layout: default
---

# Hello World

## 概要

かんたんなプログラムを実行できるようになることをめざします。


## Go Playgroundにアクセス

[https://play.golang.org/](https://play.golang.org/) にアクセスしよう。

下のような内容が表示されているかな？

```
package main

import "fmt"

func main() {
    fmt.Println("Hello, playground")
}
```



## Hello Worldにしてみよう。

プログラミングの世界では、最初にHello World（こんにちは世界）という文字をプリントアウトすることから
始めるのが定番です。

```
Hello, playground
```

を

```
Hello World
```

に修正してみよう。


# Runを押してみよう

上にRunボタンがあると思います。おしてみましょう。
Hello Worldと表示されたかな？


## Shareをしてみよう

上にあるShareボタンを押してみよう。 
リンクが出てくると思います。リンクをコピーして、Slackにペーストして、
みんなにできたのを見せてみましょう。

## ソースを分解してみてみよう


### package 

```
package main
```

golangの全てのソースコードは、package(箱)の中にある必要があります。
また、一番最初に動かすソースコードは、mainという名前にする必要があります。
だから、pacakge mainと書いてるんですね。


###  import

```
import "fmt"
```

importとは、他から持ってくるってこと。fmt っていう魔法の書に書かれている魔法を使えるように持ってきてるってことだね。
これを書かないと、fmtの魔法の書に書かれている魔法は使えないよ。

### func main

```
func main() {

    // ここにプログラムの魔法を作る

}
```

main()というのは特別な魔法で、この名前で package mainの中に作っておくと、最初に実行されるんだよ。

###  fmt

```
    fmt.Println("Hello World")
```

fmtの魔法の書には、Println() という魔法があって、これを使うと、文字を改行して表示してくれるんだよ。
これが、一番最初にみんなが、おぼえる魔法だよ。


[fmtの魔法の書原本](https://golang.org/pkg/fmt/)はここにあるよ。
[fmtの日本語の魔法の書](http://golang.jp/pkg/fmt)はここだね


## 課題

* Hello World以外の文字もいろいろ試して書いてみよう。
* fmt.Print("文字") もつかってみよう。どうなるかな？

## ヒント

* コピーは command + c 、ペーストは command + v  でできるよ


