---
layout: default
---

# interface

## 概要

interfaceについて学びます。

##  interfaceとは

型がわからない時や、混ざっている時に、interfaceという型をを使うことができます。
つまり、「なんでもあり型」ってことですね。

```
  // intとstringが混ざったsliceを作りたい
  arr := []interface{}{1,"もじ"}

 for _,i := range arr {
    fmt.Println(i)
 }

```
[サンプル](https://play.golang.org/p/yl7aUb5UZN){:target="_blank"}


## 取り出す時


型を指定して取り出すさいには、キャストする必要があります

```
// intとstringが混ざったsliceを作りたい
i := []interface{}{1, "もじ"}

// 型を指定してとりだしたい。どの型なのか教えてあげる必要があります。
var num int = i[0].(int)
var str string = i[1].(string)

fmt.Println(num,str)
```
[サンプル](https://play.golang.org/p/QEnwaZ4kMa){:target="_blank"}


## 活用例 : 引数のinterface{}対応

足し算をする時に、intでも、stringの数字にも対応してみる

```
package main

import (
        "fmt"
        "strconv"
       )

func main() {

    // 間違えて、数字の文字を渡しても動くように
    fmt.Println(Addition(3, "10"))

}

func Addition(x interface{}, y interface{}) int {

xi := 0
        yi := 0

        xs, isString := x.(string)

        if isString {
            xi, _ = strconv.Atoi(xs)
        } else {
            xi = x.(int)
        }

    ys, isString := y.(string)

        if isString {
            yi, _ = strconv.Atoi(ys)
        } else {
            yi = y.(int)
        }

    return xi + yi
}

```
[サンプル](https://play.golang.org/p/Q4LQUyuUwZ){:target="_blank"}


## 活用例 : 汎用的なmapデータ

いろいろな型をもった変数をもった、mapを使う例をみてみましょう

```
func main() {

    kuruma := GetNorimono("くるま", 300)
    hikouki := GetNorimono("ひこうき", 10000)

    fmt.Println(kuruma)
    fmt.Println(hikouki)

}

func GetNorimono(name string, omosa int) map[string]interface{} {

    return map[string]interface{}{
        "名前": name,
        "重さ": omosa,
    }

}
```
[サンプル](https://play.golang.org/p/t01ajlSc2Z){:target="_blank"}

