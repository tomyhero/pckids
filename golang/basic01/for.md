---
layout: default
---

# for

## 概要

繰り返し文を作るさいには、for を使います。

## 指定した数をくりかえしてみよう

```
var count int = 10

for i := 0; i < count ; i++ {
    fmt.Println("くりかえし",i)
}
```
[サンプル](http://play.golang.org/p/SowI9Gyxep)

### 分解してみよう

この
```
i := 0;
``` 
の部分は iという変数を0をいれて作るって意味だよ。変数のところで習ったよね。

この
```
i < count;
``` 
の部分は countより小さければという条件文だよ。if elseのところで習ったよね。

この
```
i++ 
```
の部分は、自分自身に1をたすってことだよ。別の書き方だと、

```
i = i + 1
```

これと同じ意味だよ。



## 始める数字をかえてみよう


3からはじめてみよう。どうなるかな？
始める数字は変更できるんだよ。

```
for i := 3; i < 10 ; i++ {
    fmt.Println("くりかえし",i)
}
```
[サンプル](http://play.golang.org/p/WhEuz5s1yT)


## 1ずつではなく、２ずつあげてみよう

1ずつじゃなくて、２ずつにしてみよう

```
for i := 0; i < 10 ; i=i+2 {
    fmt.Println("くりかえし",i)
}
```
[サンプル](http://play.golang.org/p/31Dgjlgvxx)

## 10からはじめて、へらしてみよう

```
for i := 10; i != 0 ; i-- {
    fmt.Println("くりかえし",i)
}
```
[サンプル](http://play.golang.org/p/OshTONLH9_)




