---
layout: default
---

# array

## 概要

リストのデータを扱う場合、array,sliceを使います。

## arrayとsliceの違い

* 複数のものを格納することができ、格納できる数が最初からきまっているのが、array.
* 複数のものを格納することができ、格納できる数が決まっておらず、足したり減らしたりできるのがslice.


## arrayの作り方

10この数字のリストを作ってみよう。サンプルで、１０個できてるのを確認しよう。

```
var numbers [10]int

// 省略での書き方。上のと同じ意味。
numbers := [10]int{}

// 初期データを設定。
numbers := [10]int{1,2,3}

```
[サンプル](http://play.golang.org/p/Jm1ehYgr10)

arrayの紹介はここまでで基本的に配列を作る時は、sliceを使っていきます。

## sliceの作り方

sliceを作ってみよう。

```
var numbers []int 

// 省略での書き方。上のと同じ意味。
numbers := []int{}

// 初期データを設定。
numbers := []int{1,2,3}

```
[サンプル](http://play.golang.org/p/M12vEuwKP0)


## 配列に一つずつにアクセスしてみよう

```

numbers := []int{1,2,3}

fmt.Println(numbers[0])
fmt.Println(numbers[1])
fmt.Println(numbers[2])

```
[サンプル](http://play.golang.org/p/4jZJrM33Vf)


もっと、かっこよくアクセスしてみよう。 
len() を使うと、配列の数をとることができるよ

```
numbers := []int{1, 2, 3}
for i := 0; i < len(numbers); i++ {
  fmt.Println(numbers[i])
}
```
[サンプル](http://play.golang.org/p/KkbdrVElky)

さらにかっこよく、アクセスしてみよう。rangeというのを使うと、
配列がなくなるまで、繰り返すことができるよ。

```
numbers := []int{1, 2, 3}
for i := range numbers {
  fmt.Println(numbers[i])
}
```
[サンプル](http://play.golang.org/p/GZHvGdTibu)


## 配列に数字を追加してみよう

```

numbers := []int{1, 2, 3}
numbers = append(numbers,8) // {1,2,3,8} になる

```
[サンプル](http://play.golang.org/p/e48PQQ-qMK)

## 配列から値を削除してみよう

[:]をつかって、取り出すことができます。

```
numbers := []int{1, 2, 3}

// 最初から、二つ目までをとりだして、入れ直す
numbers = numbers[0:2]


```
[サンプル](http://play.golang.org/p/VF4jQzkDBp)
