# 概要
リモートにプッシュする前にローカルでビルドして見栄えを確認するための環境構築方法です。

ここではjekyllのデフォルトのひな形を適用していますが、Github Pagesのデフォルトテーマをローカルでビルドする方法も見つけたのでリンクを残しておきます。

以下に手順を書いていますが、もしかしたら[ここ](https://help.github.com/ja/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll)だけで完結したかも...

### 用語
* [GitHub Pages](https://help.github.com/ja/github/working-with-github-pages/about-github-pages)
* [GitHub PagesとJekyll](https://help.github.com/ja/github/working-with-github-pages/about-github-pages-and-jekyll):GitHub Pagesに組み込まれている静的サイトジェネレータ

# 目次
[TOC]

# 準備
## リポジトリの準備

GithubにPagesで公開する用のリポジトリを作成し、ローカルにクローンします。

※既存のリポジトリに追加してもいいのですが、既存リポジトリがprivateの場合Pagesを公開するためには課金する必要があるため。

## 環境構築
[この通りです](https://help.github.com/ja/github/working-with-github-pages/testing-your-github-pages-site-locally-with-jekyll)
ただ、「サイトをローカルでビルドする」 の「3 ローカルで Jekyll サイトを実行します.」がうまくいかないです。

なので
[この](http://jekyllrb-ja.github.io/tutorials/using-jekyll-with-bundler/#bundler%E3%81%AE%E8%A8%AD%E5%AE%9A)通りにしました

以降の編集には
[この](https://howpon.com/9443)情報が役立ちそう

その結果もともとのGitHub Pages用のjekyllのテーマは消し飛ばされています。
多分上記のリンクの「jekyll骨格を作成する」の項目をスキップし、
jekyllのテーマを使うための設定をしてあげれば良さそうです。
[このサイト](https://sakanasoft.net/github-pages-by-localhost/#install_github_pages_gem)が参考になりそう



