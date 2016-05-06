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



## 値渡しと参照渡し

structを引数として渡すときに、値渡しというやり方と、参照わたしというやり方があります。


値で渡すと、同じものをコピーして渡します。参照で渡すと、じゅうしょだけを教えて、値は渡しません。


```
// のりものの struct だよ
type Norimono struct {
    Name      string
        Toberu    bool
        Hashireru bool
        Ukaberu   bool
        Oto       string
}

func main() {

    // 魂をいれる
    kuruma := Norimono{Name: "くるま", Toberu: false, Hashireru: true, Ukaberu: false, Oto: "プップー"}

    Hensin(kuruma)
    fmt.Println(kuruma.Name)

    SugoiHensin(&kuruma)
    fmt.Println(kuruma.Name)

}

// 値渡し
func Hensin(n Norimono) {
    n.Name = "スポーツカー"
}

// 参照渡し
func SugoiHensin(n *Norimono) {
    n.Name = "スポーツカー"
}


```
[サンプル](https://play.golang.org/p/_IInm0moIY){:target="_blank"}
