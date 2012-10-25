# my\_middleman powered by Middleman

my\_middleman は 静的サイト・ジェネレータ [Middleman](https://github.com/middleman/middleman) のテンプレートエンジンを [slim](https://github.com/stonean/slim) に設定したものです。  
提携するマークアップエンジニアさんやコーダーさんと同じ環境で作業できるように github で管理しています。

## メリット

- html 全体の基本構造を Layout として管理できる
- html の個別の共通部分( ex.nav ) を partial として管理できる
- slim を使用することで, タイプ数を減らすことができる
- slim 以外のテンプレートにも対応( ex.haml )
- css を scss や sass で記述できる


## デフォルト設定との違い

- テンプレートエンジンに slim を設定
- layout.slim と index.html.slim を作成
- CSS 管理ディレクトリを stylesheets から css へ変更
- JavaScript 管理ディレクトリを javascripts から js へ変更
- helpers ディレクトリ以下にPageヘルパを用意しメソッドを実装


## 使い方

middleman を使用するには Ruby の開発環境が必要です。

### 環境用意

- gem install bundler
- gem install middleman 
- mkdir PROJECT\_DIR
- cd PROJECT\_DIR
- git init
- git pull git://github.com/yterajima/my\_middleman.git 
- bundle install --path vendor/bundler
- bundle exec middleman server

### 基本操作

- サーバ起動: bundle exec middleman (server) // _server_ を付けなくてもOK 
- HTML の生成: bundle exec middleman build

middleman に用意されているコマンドは _init_, _server_, _build_ の3種類。  
bundler経由で処理を行うため, _bundle exec middleman COMMAND_ で実行する必要があります。

このリポジトリを使用することで, 実際に使用するコマンドは2つに限定されます。

### 命名規則

- html を slim で作成する場合, _filename.html.slim_ として保存
- css を scss で作成する場合, _filename.css.scss_ として css ディレクトリに保存
- JavaScript を CoffeeScript で作成する場合, _filename.js.coffee_ として js ディレクトリに保存

## 参考

- slim の記法: [Documentation for stonean/slim
  (master)](http://rdoc.info/github/stonean/slim)
- Middleman を使ったテンプレートや Partial の使い方: [Middleman: Template, Layouts &
Partials](http://middlemanapp.com/templates/templates-layouts-partials/)

