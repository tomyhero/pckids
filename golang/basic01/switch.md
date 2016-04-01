---
layout: default
---

# switch

## 概要

if以外にも、条件分岐をできる方法があり、その方法のswitchをマスターしていきましょう。

## 簡単な例

```
    var number int = 3

    switch {
        case 1 == number:
            fmt.Println("1だよ")
        case 2 == number:
            fmt.Println("2だよ")
        case 3 == number:
            fmt.Println("3だよ")
        case 3 <= number:
            fmt.Println("3以上だけど、3のときはこないよ")
        default :
            fmt.Println("それ以外")

    }

    // 上のswitch文と同じ動きをするよ
    if number == 1 {
        fmt.Println("1だよ")
    } else if number == 2 {
        fmt.Println("2だよ")
    } else if number == 3 {
        fmt.Println("3だよ")
    } else if number <= 3 {
        fmt.Println("3以上だけど、3のときはこないよ")
    } else {
        fmt.Println("それ以外")
    }

```
[サンプル](http://play.golang.org/p/DryaM0AL2w)
