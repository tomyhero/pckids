---
layout: default
---

# Golang基本1コース - funcの練習問題

## 概要

1問1点で、8問出題され8点満点です。
答えは1問ずつ、先生に個別チャットで送ってください。

## 問題集

### 問題1

以下の関数を実行してください。

```
func Kick(){
    fmt.Println("キック")
}
```

### 問題2

以下の関数を実行し、「こんにちは、たけし君」と表示させなさい。
また、そのあとに、「こんにちは、たろう君」と表示させなさい。

```
func Hello(name string){
    fmt.Println("こんにちは、" + name + "君")
}
```

# 問題3

以下の関数を実行し、戻り値を受け取りなさい。また、
受け取った値を表示しなさい。

```
func Name() string {
    return "たけし"
}

```

# 問題4

以下の関数をつかい、0から9まで表示しなさい。
また、for を使いなさい。

```
func Display(i int){
    fmt.Println(i)
}

```

# 問題5

「こんにちは」と表示する関数を作成し、実行しなさい。

# 問題6

以下のソースを実行すると13と表示されるように、
Addition関数を作りなさい

``` 
answer := Addition(3,10)
fmt.Println(answer)
```

# 問題7

ColorNameという関数を作成し、"aka"を渡すと「赤色です」"ao"を渡すと「青色です」
と表示させなさい。

``` 
fmt.Println(ColorName("aka"))
fmt.Println(ColorName("ao"))
```

# 問題8

自分で考えた関数を作成し、実行してみてください。
