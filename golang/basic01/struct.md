---
layout: default
---

# struct

## 概要

自分で特別な型を作りたい時に、structをつかいます


## 簡単な sturctを作ってみよう


のりものの情報をもった、struct Norimono を試しに作ってみます。


```

// のりものの struct だよ
type Norimono struct {
    Name string
        Toberu bool
        Hashireru bool
        Ukaberu bool
        Oto string
}

func main() {

// structにくるまの魂をいれるよ
kuruma := Norimono{
Name : "くるま",
     Toberu : false,
     Hashireru : true,
     Ukaberu : false,
     Oto : "プップー",
        }

// structにひこうきの魂をいれるよ
hikouki := Norimono{
Name : "ひこうき",
     Toberu : true,
     Hashireru : false,
     Ukaberu : false,
     Oto : "フューン",
         }


// structにふねの魂をいれるよ
fune  := Norimono{
Name : "ふね",
     Toberu : false,
     Hashireru : false,
     Ukaberu : true,
     Oto : "ボー",
       }

fmt.Println(kuruma.Name)
fmt.Println(hikouki.Name)
fmt.Println(fune.Name)

}

```
[サンプル](https://play.golang.org/p/SpWVb4kZSB){:target="_blank"}


## のりものを走らせてみよう


structには、関数をはやすことができます。
ためしに、はしるという関数を追加してみましょう。

```
// のりものの struct だよ
type Norimono struct {
    Name      string
        Toberu    bool
        Hashireru bool
        Ukaberu   bool
        Oto       string
}

func (n Norimono) Hasiru() {

    if n.Hashireru {
        fmt.Println(n.Name, "ははしるよ！", n.Oto)
    } else {
        fmt.Println(n.Name, "ははしれないよ...")
    }

}

func main() {

    // 魂をいれる
    kuruma := Norimono{Name: "くるま", Toberu: false, Hashireru: true, Ukaberu: false, Oto: "プップー"}
    hikouki := Norimono{Name: "ひこうき", Toberu: true, Hashireru: false, Ukaberu: false, Oto: "フューン"}
    fune := Norimono{Name: "ふね", Toberu: false, Hashireru: false, Ukaberu: true, Oto: "ボー"}

    kuruma.Hasiru()
    hikouki.Hasiru()
    fune.Hasiru()

}
```

[サンプル](https://play.golang.org/p/sAXjfGIXZC){:target="_blank"}

サンプルに、Tobu,Kogu という関数を生やしてみよう




