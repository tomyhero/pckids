---
layout: default
---

# func

## 概要

関数の理解を深め、利用、作成っできることを目指します

## 関数とは

簡単に言うと、魔法のようなものです。
これまでに、よくでてきた、fmt.Println() も関数です。

```
fmt.Println("こんにちは")
```
これを実行すると、「こんにちは」ってかかれますよね？

こういった魔法（関数）は、使うだけじゃなくて自分で作ることももちろんできます。

## 作ってみよう

試しに、色の名前を表示するという魔法を作ってみましょう。

```
func main(){
    PrintColor("aka")
    PrintColor("ao")
}

func PrintColor(color string){
   if color == "aka" {
        fmt.Println("赤色")
   } else if color == "ao" {
        fmt.Println("青色")
   } else {
        fmt.Println("黒色")
   }
}

```
[サンプル](http://play.golang.org/p/ltXleaMNWA)


## 引数

魔法（関数）を唱える時に、何かを渡すことができます。PrintColorの場合 "aka"
とかを渡していますね。これを、引数と言います。
引数はなくてもいいし、たくさんあっても大丈夫です。
引数を有効に使うと、使い回しができるようになります。

```

// 引数なし
func Fire(){
    fmt.Println("ファイアー！")
}

// 引数なしでの足し算。3 + 3 しかできない
func AdditionThreePlusThree(){
    fmt.Println("x + y = ", 3 + 3 )
}

// 引数を使うと、いろいろな足し算ができるようになったね！
func Addition(x int, y int){
    fmt.Println("x + y = ", x + y )
}

```
[サンプル](http://play.golang.org/p/c7HOQclaFY)

## 戻り値

魔法(関数)を唱えたあとに、何かを手にいれれるようにすることができます。
それが、戻り値です。何個でも手に入れれるようにすることができます。


```

func Banana() string {
    return "ばなな"
}

// 2個でもできるよ
func Fruits() ( string,string){
    return "ばなな","りんご"
}

// 引数ありで、戻り値ありもできるよ
func Addition(x int, y int) int {
    return x + y
}

```
[サンプル](http://play.golang.org/p/465ORCnNs4)


## 使ってみよう

すごい魔法使いたちが作った、魔法がすでにたくさんあるので、
いくつかためにし使ってみよう


### ランダムな数字を作る

```
package main 

import (
    "fmt"
    "math/rand"
)

func main(){
   
   num := rand.Intn(100)
   fmt.Println( num )

   fmt.Println( rand.Intn(100) )
   fmt.Println( rand.Intn(100) )
   fmt.Println( rand.Intn(100) )
   fmt.Println( rand.Intn(100) )

}
```
[サンプル](http://play.golang.org/p/beVCTvEOgg)

### 時間を表示する

```
package main

import(
    "fmt"
    "time"
)

func main(){

    fmt.Println(time.Now())

}

```
[サンプル](http://play.golang.org/p/QfZY2J8_A0)


## 練習問題

[練習問題](./practice/func)
