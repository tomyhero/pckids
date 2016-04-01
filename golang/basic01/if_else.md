---
layout: default
---

# 基本変数

## 概要

if else を使った条件分岐を扱えるようになろう

ifは、英語なんだけど、日本語だと「もし〜だったら」という意味だよ

## if


ifのあとに条件をかいて、条件にマッチすれば実行されます。

```
if true {
    fmt.Println("これは表示されるよ")
}

if false {
    fmt.Println("これは表示されないよ")
}

if 1 == 1 {
    fmt.Println("これは表示されるよ")
}

if 1 == 2 {
    fmt.Println("これは表示されないよ")
}

if "チューリップ" == "チューリップ" {
    fmt.Println("これは表示されるよ")
}

if "チューリップ" == "ヒマワリ" {
    fmt.Println("これは表示されないよ")
}
```

* [サンプル1](http://play.golang.org/p/kAnIlTuvbP)


## 条件の書き方

### 同じ場合 ( == )

=を個並べると、同じだったらという意味になります。

同じタイプしかくらべることはできないよ。例えば、数字と文字は比べれないよ。

```
var name string = "じばニャン"
var number int = 3
var moji_number  string = "3"

if name == "じばニャン" {
    fmt.Println("これは表示されるよ")
}

if number == 3 {
    fmt.Println("これは表示されるよ")
}

if moji_number == "3" {
    fmt.Println("これは表示されるよ")
}

// これは、文字と数字だからできないよ
// if name == number { }

// これも、文字と数字だからできないよ。
// if name == moji_number { }

```
[サンプル](http://play.golang.org/p/M0ZH96KOI2)


### 違う場合 ( != )


!= をつがうと、同じじゃない場合をしらべれるよ！

```
var name string = "じばニャン"
var number int = 3
var moji_number  string = "3"

if name != "ロボニャン" {
    fmt.Println("これは表示されるよ")
}

if number != 1 {
    fmt.Println("これは表示されるよ")
}

if moji_number  != "1" {
    fmt.Println("これは表示されるよ")
}

```
[サンプル](http://play.golang.org/p/BgWSVJ2qh_)

### 数字の大きさを比べる場合 ( <,>,=<,>= )

数字の大きさで比べる時は < , >,  =< , >= を使うことができます。

```
var number int = 3

// 3 は 4よりちいさい
if number < 4 {
    fmt.Println("これは表示されるよ")
}

if number <= 3 {
    fmt.Println("これは表示されるよ")
}

if number <= 4 {
    fmt.Println("これは表示されるよ")
}

if number > 2 {
    fmt.Println("これは表示されるよ")
}

if number >= 3 {
    fmt.Println("これは表示されるよ")
}

if number >= 4 {
    fmt.Println("これは表示されるよ")
}

```

[サンプル](http://play.golang.org/p/zJKS36h_w9)

## else 

elseは英語で、日本語で言うと「それ以外」という意味だよ。

```

var number int = 3

if number == 2 {
    fmt.Println("numberは2だね")
} else {
    // 2以外はぜんぶここにくる
    fmt.Println("numberは2以外だね")
}

```
[サンプル](http://play.golang.org/p/b9H3PQfmV8)


## if else 

if分を何個も続けたい時は、if else をつかうんだよ
if elseは、「それ以外にもし〜なら」って意味だよ

```

var number int = 3

if number == 1 {
    fmt.Println("numberは1だね")
} else if number == 2 {
    fmt.Println("numberは2だね")
} else if number == 3 {
    fmt.Println("numberは3だね")
// else はそれ以外、だから、かならず最後に書く必要があるよ
} else  {
    fmt.Println("numberは1と２と３以外だね")
}


// ブロックを別にすれば、elseじゃなくて、
// また、ifからだよ
if number == 3 {
    fmt.Println("numberは3だね")
}else {
    fmt.Println("numberは3以外だね")
}


```
[サンプル](http://play.golang.org/p/npD5k0weT8)


## ヒント

* { はかならず } で閉じる
* ( はかならず ) で閉じる
* " はかならず " で閉じる

## 参照

- A Tour of Go: [If](https://go-tour-jp.appspot.com/flowcontrol/5)
- A Tour of Go: [If with a short statement](https://go-tour-jp.appspot.com/flowcontrol/6)
- A Tour of Go: [If and else](https://go-tour-jp.appspot.com/flowcontrol/7)

