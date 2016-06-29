reveal.js Template
------------------

reveal.js でスライドを作るためのテンプレート



### 起動方法

```
$ npm install
$ npm start
```

を実行すると、ローカルサーバーが http://localhost:8000 で起動するのでブラウザで開く。

スライドの内容は index.md に記述する。


### スライドテーマの変更

スライドの CSS は index.html の

```
<!-- Slide Theme -->
<link rel="stylesheet" href="css/theme/black.css">
```

の部分を、`css/theme` ディレクトリ以下の好きなテーマファイルに置き換える。



### PDF 化

http://localhost:8000/?print-pdf/#/ にアクセスし、ブラウザの印刷機能を使用する。



### Markdown ファイルの追加

index.html の `<div class="slides">...</div>` に

```html
<section data-markdown="./foo.md"
         data-separator="^\n\n\n"
         data-separator-vertical="^\n--\n"
         data-separator-notes="^Note:">
</section>
```

を追加すると、複数の Markdown ファイルを読み込むことができる。
