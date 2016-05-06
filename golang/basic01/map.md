---
layout: default
---

# map

## 概要

辞書のように変数を保持するのに、mapを使います

## mapとは

辞書で例えば、「ひこうき」を調べたい場合、「ひこうき」の項目を調べますよね。
そのような、形で情報を保持できるのが、mapです。

実際に使っている、例をみてみましょう。

```
norimono := map[string]string{
    "ひこうき" : "ひこうきは、そらをとぶのりものです",
    "くるま" : "くるまは、じめんをはしるのりものです",
    "ふね" : "ふねは、かわや、うみのうえをはしるのりものです",
}

fmt.Println( norimono["ひこうき"] )
fmt.Println( norimono["くるま"] )
fmt.Println( norimono["ふね"] )

```
[サンプル](https://play.golang.org/p/4wIeTltAoo){:target="_blank"}


## mapの作り方

mapを作るのはとても簡単です。４つのセクションがあります。

1. 最初に「map」とかく
2. 次に、辞書をひくときの「[型]」をかく
3. 次に、辞書がもっている「型」をかく
4. つぎに、{} をかく。中身も登録したい場合は、{} の中に情報をかく。


実際に、例をみてみましょう。

```

 // 文字で辞書を引き、文字をみつけるとき
 norimono := map[string]string{
    "ひこうき" : "ひこうきは、そらをとぶのりものです", 
 }

 fmt.Println(norimono["ひこうき"])

 // 数字で辞書を引き、文字をみつけるとき
 food := map[int]string{
    1 : "カレーライス",
    3 : "うどん",
 }

 fmt.Println(food[1])

 // 数字で辞書を引き、数字をみつけるとき
 number := map[int]int {
    1 : 10,
    30 : 500,
 }

 fmt.Println(number[1])

 // 文字で辞書を引き、数字をみつけるとき

 color := map[string]int {
    "あか" : 1,
    "あお" : 30,
 }

 fmt.Println(color["あか"])


```


[サンプル](https://play.golang.org/p/iTSUlZxOQZ){:target="_blank"}

## mapへの追加、変更

すでに作られたmapに、データを追加したり、上書きしたりすることができます。


```
    norimono := map[string]string {
        "ひこうき" : "じめんをもぐるのりもの",
    }

    // 治すことができる
    norimono["ひこうき"] = "そらをとぶのりもの";

    // 追加することができる
    norimono["くるま"] = "じめんをはしるのりもの";

    fmt.Println(norimono)

```
[サンプル](https://play.golang.org/p/zQvyGOYEYv){:target="_blank"}

## mapからの削除

すでに作られたmapから、データを削除することができます。

```
    numbers := map[int]int {
        1 : 10,
        30 : 100,
        43 : 354,
    }
    
    delete(numbers,30)
    fmt.Println(numbers)

```
[サンプル](https://play.golang.org/p/rXL7o0PDYD){:target="_blank"}

## mapが、あたいをもってるかのチェック

mapが、指定したあたいを持っているかをチェックすることができます。


```

    norimono := map[string]string{
        "ひこうき" : "ひこうきは、そらをとぶのりものです",
    }

    
    // _ は、値を捨てるってこと。
    _,has_hikouki := norimono["ひこうき"]


    if has_hikouki {
        fmt.Println("ひこうきはある")
    }else {
        fmt.Println("ひこうきはない")
    }


    _,has_kuruma := norimono["くるま"]

    if has_kuruma {
        fmt.Println("くるまはある")
    }else {
        fmt.Println("くるまはない")
    }


```

[サンプル](https://play.golang.org/p/gMD50tTLh0){:target="_blank"}















