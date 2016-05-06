---
layout: default
---

# install_go

## 概要

自分のアカウントに、go をインストールしてみよう。今回は[gvm](https://github.com/moovweb/gvm)を使います。

## 手順

### 1. ターミナルを起動します

ランチパッドの中に、その他の項目があります。その中にターミナルがあるので起動します。

### 2. gvmのインストール

以下の処理を実行( xcode,brew等のインストールが先に必要かも... )
```
bash < <(curl -s -S -L https://raw.githubusercontent.com/moovweb/gvm/master/binscripts/gvm-installer)
```

### 3. goのインストール

以下の処理を実行
```
gvm install go1.4 -B
gvm use go1.4
export GOROOT_BOOTSTRAP=$GOROOT
gvm install go1.6
gvm use go1.6
```


### 4. goの起動

Goのversionを表示させてみましょう。1.6と表示されれば成功です
```
go version
```

### 5. ログイン時の読み込み

```
echo "gvm use go1.6" >> ~/.bashrc
```


