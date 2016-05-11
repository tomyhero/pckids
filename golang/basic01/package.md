---
layout: default
---

# package

## 概要

packageの使い方を学びます


## packageを作ってみる

packageを作るのは、palyground ではできません。
ターミナルを使って作業していきます。

### 手順１ ディレクトリ(package)作成


packageは、ディレクトリ名と同じです。
goのパッケージは $GOPATH で設定されている場所に保存する必要があります。


今回は、hello_packageというパッケージを作り、その中で作業をしていきます。
また、その親パッケージとして project というのを作り、そのあとに、hello_package配下に移動します。


ディレクトリを作成します

```
mkdir -p ${GOPATH}/src/project/hello_package
```

ディレクトリの中に移動します

```
cd ${GOPATH}/src/project/hello_package
```

現在地の確認

```
pwd
```

### 手順２ プログラムファイル、ディレクトリを作ります

プログラムをおいてみます。
ディレクトリ構造はこうります。

```
.
├── main.go
└── norimono
    └── norimono.go
````

ディレクトリ構造だけをまず作ってみましょう。

```
touch main.go
mkdir norimono
touch norimono/norimono.go
```

treeコマンドで構造を確認してみます
(treeコマンドがインストールされている必要があります)

```
tree 
```

### 手順3 norimono.go のプログラムを書きます


好きなEditorを使って、 ```norimono/norimono.go``` にプログラムを書きます。


```
// packageは、ディレクトリ名と同じである必要があります。
package norimono

import (
        "fmt"
       )

type Norimono struct {
    Name string
}

func (n Norimono) SayName() {
    fmt.Println(n.Name + "だよ")
}

```

### 手順4 main.go のプログラムを書きます


好きなEditorを使って、 ```main.go``` にプログラムを書きます。

```
package main

import (
        // 自分で作った、パッケージを読み込みます
        "project/hello_package/norimono"
       )

func main() {
    // 自分で作った、パッケージのstructを呼び出します
    kuruma := norimono.Norimono{Name: "くるま"}
    kuruma.SayName()
}

```

### 手順4 実行してみよう


ターミナルから、次のコマンドを実行します

```
go run main.go
```

「くるまだよ」と表示されたかな？


