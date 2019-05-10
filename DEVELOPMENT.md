# GoLang開発まとめ

## 検討要素一覧

GoLangにてWebシステムを開発するために整理しておかなければならないものをリストアップする。
それぞれの整理する要素に対して何に関するものかをチェックした表となる。

|要素|仕様|MK|UT|SI|CI|CD (Dev)|CD (Pro)|
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|[IDE](#IDE)||x||||||
|[GoLangバージョン管理](#GoLangバージョン管理)||x|||||
|[パッケージ管理（利用）](#パッケージ管理（利用）)||x|x|x||||
|[パッケージ管理（内部管理）](#パッケージ管理（内部管理）)||x|x|x||||
|[ビルドシステム](#ビルドシステム)||x|x|x||x|x|
|[フレームワーク](#フレームワーク)||x||||||
|[静的解析](#静的解析)|||x||x|||
|[テストフレームワーク](#テストフレームワーク)|||x||x|||
|[Mockフレームワーク](#Mockフレームワーク)|||x||x|||
|[カバレッジ](#カバレッジ)|||x||x|||
|[OAS3（ソースコード）](#OAS3（ソースコード）)||x||||||
|[OAS3（スタブ）](#OAS3（スタブ）)|||x|x||||
|[OAS3（ドキュメント）](#OAS3（ドキュメント）)|x|||||||
|[CIシステム](#CIシステム)||x|x||x|||

---

## 参考資料

|リンク|概要|
|:---|:---|
|[Go言語 文法まとめ](https://qiita.com/rock619/items/db44507d02814e490902)|文法がまとまっている|
|[実践Go言語](http://golang.jp/effective_go)|構文＋言語仕様説明|

---

## IDE
- `VSCode` + `Go` プラグイン
- 無償で他あれば検討

---

## GoLangバージョン管理
固定とするならば、msi等のインストローラでも構わないように思える。  
それなりに言語としてのアップデートも激しい模様。  

- goenv
  - `git clone`でインストール

---

## パッケージ管理（利用）

GoLangに含有されている。  
ここ数年で大分揺れている。  
以下遷移も含めて一覧となる。  

- go get
- vgo
- Module

---

## パッケージ管理（内部管理）

開発用の内部パッケージの管理方法。  
`Module` については `git` で `clone`するのが通例のようなので、
そういう意味だとGitLabがあればいいのか？  
あとは、`go mod` コマンドのリポジトリの向け先を変えることができればOK？

---

## ビルドシステム

GoLangに含有されている。  
Java（jar|war|ear|fatjar）やNode.js（bundle.js）のようなアーカイブは不要っぽい。  
パッケージ参照を行って、自前ビルドするだけ？

そのため、`Gradle`、`Maven`、といったビルドシステム的な位置付けのものは存在しないと思われる。  
要継続調査

---

## フレームワーク

Webアプリケーションを構築するためのフレームワークに特化して検討する。  
また、優先すべきアプリ形態としてはREST-APIとなる。




---