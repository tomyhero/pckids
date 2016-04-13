---
layout: default
---

# block

## 概要

blockとは文字や、プログラムを入れたりする箱のようなものです

## ブランケット {}

ソースコードを整理するために、入れる箱です。箱の中には箱をいれることができます。
{ ではじまって、かならず } で閉じる必要があります。
{ } の中で作られた、変数は {} の外では使うことができません。

```
package main

import "fmt"

func main(){ // これが main関数の箱の始まり

    { // 箱A開始

        i := 1 // この変数は、箱Aの中だけでつかえるよ
        fmt.Println(i)

    } // 箱A終了

    if true { // trueの箱

        // trueの時のプログラミングをこの箱の中にかく


    // trueの箱はここまで
    } else { // falseの箱

        // falseの時のプログラミングをこの箱の中にかく

    } // falseの箱はここまで


}  // これがmain関数の箱の終わり


```
[サンプル](http://play.golang.org/p/e1nZ8bgI9s)

## ダブルクォーテーション ""

文字を使いたい時は、""で挟む必要があります

```

s := "もじだよ"

```

## かっこ ()

関数の引数の受け渡しに使います。()の中にいれたのを、関数にわたすことができます。

```
func main() {
    // 関数を呼び出すときに、引数をかっこで挟むよ
    answer := add(10,12) 

    // これもかっこで渡してるね
    fmt.Println(answer)
}

// かっこで受け取る予定、引数を宣言するよ
func add( x int , y int ) int {
    return x + y
}


```

[サンプル](http://play.golang.org/p/Chbj3su4hV)
