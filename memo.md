# Microservices AntiPatterns and Pitfalls (ja_JP)

Mark Richards著「Microservices AntiPatterns and Pitfalls」の翻訳プロジェクトです。  
この翻訳プロジェクトは[Gitbook](https://www.gitbook.com/ "Gitbook")を使用して翻訳したドキュメントを作成していきます。

## Gitbook インストール手順

前提としてNodeはインストールしておく

* コマンドプロンプトより以下のコマンドを実行        

```bash
npm install -g gitbook
npm install -g gitbook-cli
```

* インストール後、Gitbookがインストールされたか確認     

```bash
gitbook --version
```

## プラグインインストール
プロジェクトクローン後、Gitbookプラグインをダウンロードするにはドキュメントホーム[^*]で以下のコマンドを実行する。
```
gitbook install
```

## プレビュー
ローカルホストでドキュメントの確認を行う場合はドキュメントホーム[^*]で以下のコマンドを実行する。
```
gitbook serve
```
完了後、http://localhost:4000 にアクセスすると生成されたドキュメントを確認できる。

## Webページ作成 
ドキュメント作成後、ドキュメントホーム[^*]で下記コマンドを実行し、ビルドを行う。
```
gitbook build
```

## PDF作成
#### ①	Calibreのインストール
下記URLからCalibreをダウンロードしインストールする。
http://calibre-ebook.com/download

#### ②	PDFを作成する。
ドキュメントホーム[^*]で下記コマンドを実行し、PDFを作成する。
```
gitbook pdf
```
コマンド実行後、book.pdfが作成される。
上手くいかない場合はコマンドプロンプトを再起動して、再度コマンドを実行する。

[^*]: book.jsonのある場所
