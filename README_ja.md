# 403bypasser
403レスポンスコード回避の手順を自動化するツールです。

## Description 
多くの#bugbountytipsに403レスポンスコードを回避する方法が書かれているので、すべてのメソッドを集めてみると、すべてのメソッドを処理するために40以上のリクエストが必要なことがわかりました。 そこで、私は自動化が好きなので、重い仕事をするためにこのツールを作りました。

このツールは、403レスポンスコードを回避するために3つのテクニックを使用し、各リトライのレスポンスコードを読みやすいようにカラー出力で表示します。

1. 複数のリクエストメソッドを使用する ( GET - POST- HEAD... etc)

2. URLの末尾に複数のペイロードを使用する (kudos to those who tweet these tips)

3. リクエストにヘッダを追加する (X-Forwarded-Host , X-Host ... etc )

## インストール :
```
sudo apt update && sudo apt install python3-pip
git clone https://github.com/smackerdodi/403bypasser.git
cd 403bypasser
pip3 install -r requirements.txt
```

## 使用方法 :

このツールは url と path の2つの引数を取ります。

`python3 403bypasser.py url path`

<dl>
    <dt>使用例 :</dt>
    <dd><code>python3 403bypasser.py https://www.example.com /admin</code> ( urlとpathの間のスペース )</dd>
</dl>

## Todo :

このツールは複数のスレッドを処理し、1つのURLだけでなく、URLのリストを取るようにします。
