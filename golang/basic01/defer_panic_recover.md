---
layout: default
---

# defer_panic_recover

## 概要

defer,panic,recoverの使い方を学びます

## deferの使い方


関数の処理がすべて終わった時に、実行させることができます。


```
func main() {
    Fire()
}

func Fire() {
    defer fmt.Println("ファイアー成功!")
    defer fmt.Println("ファイアー終わり！")
    fmt.Println("ファイアー!")
}
```
[サンプル](https://play.golang.org/p/l9E20Sd8Wo){:target="_blank"}


## panicの使い方

強制的にプログラムを中断させることができます！
ただし、中断しても、deferは動きます。

```
func main() {
    Fire()
    fmt.Println("絶対こない")
}

func Fire() {
    defer fmt.Println("Fire終了！")

    panic("MPが足りない！")

    //これは実行されない
    fmt.Println("ファイアー!")
    fmt.Println("絶対こない")

}
```
[サンプル](https://play.golang.org/p/kBOCk8i_Ss){:target="_blank"}

## recoverの使い方

recoverを使うと、panicを防ぐことができます。

お薬で、パニックを治す感じですね。


```

func main() {
    Fire()
        fmt.Println("絶対くる！")

}

func Fire() {

    defer func() {
        fmt.Println("Fire終了！")
        err := recover()
        if err != nil {
            fmt.Println("回復!")
        }
    }()

    panic("MPが足りない！")

    //これは実行されない
    fmt.Println("ファイアー!")
    fmt.Println("絶対こない")

}



```

[サンプル](https://play.golang.org/p/cBvvC8vQ4O){:target="_blank"}
