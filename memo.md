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
プロジェクトクローン後、Gitbookプラグインをダウンロードするにはコンテンツホーム[^*]で以下のコマンドを実行する。
```
gitbook install
```

## プレビュー
ローカルホストでコンテンツの確認を行う場合はコンテンツホーム[^*]で以下のコマンドを実行する。
```
gitbook serve
```
完了後、http://localhost:4000 にアクセスすると生成されたコンテンツを確認できる。

## Webページ作成 
コンテンツ作成後、コンテンツホーム[^*]で下記コマンドを実行し、ビルドを行う。
```
cd C:\GitBook
gitbook build
```

## PDF作成
#### ①	Calibreのインストール
下記URLからCalibreをダウンロードしインストールする。
http://calibre-ebook.com/download

#### ②	PDFを作成する。
コンテンツホーム[^*]で下記コマンドを実行し、PDFを作成する。
```
gitbook pdf
```
コマンド実行後、book.pdfが作成される。
上手くいかない場合はコマンドプロンプトを再起動して、再度コマンドを実行する。


[^*]: book.jsonのある場所
