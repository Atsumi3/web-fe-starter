# web-fe-starter

Webフロントエンドの環境を整える。
自分の勉強のために作成

## 準備
zipをダウンロードするか、git clone をして npm install を走らせてください

## 対応
- webpack
  - 複数のコードやスタイルシートをまとめてくれるもの (a.js + b.js => c.js 的な)
  - 下記のライブラリと連携して一連の変換処理を管理してくれる
- babel (babel-loader, @babel/core, @babel/preset-env)
  - 新しいJavaScript, ECMAScript を、古い環境でも実行できるように変換してくれる
- css (css-loader, mini-css-extract-plugin)
  - 複数のCSSをまとめてくれる
- optimize-css-assets-webpack-plugin
  - CSSのminifyを助けてくれる
- sass (node-sass, sass-loader)
  - sass で書かれたスタイルをCSSにトランスパイルしてくれる
- typescript (ts-loader, typescript)
  - TypeScriptで書かれたコードをjsにトランスパイルしてくれる
  
## npmスクリプト
内容はpackage.jsonに記載
package.json がある場所で コマンドプロンプト(Windows), ターミナル(Mac) から打つ

### build-dev
```shell
npm run build-dev
```

諸々コードやスタイルシートを変換して、app/gen に出力してくれる
確認のたびに都度走らせる

### build-prod
```shell
npm run build-prod
```

諸々コードやスタイルシートを変換して、app/gen に出力してくれる
コードはminifyされて、余計な空白や文字量が削られる (容量が軽くなる)
リリースの時にはこれを走らせる
