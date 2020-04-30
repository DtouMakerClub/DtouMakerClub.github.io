---
layout: post
title:  "最初にやったことメモとサイトのメンテ方法"
date:   2020-04-30 22:56:09 +0900
categories: maintenance
---

## 最初にやったこと
### ローカルでビルドする環境を構築
このサイトの[必要な環境](https://help.github.com/ja/github/working-with-github-pages/testing-your-github-pages-site-locally-with-jekyll#prerequisites)のところ。

これでビルドするツールがそろう

### 公開用のリモートリポジトリをクローン
クローンする

ビルドしたとき、いろいろなものが混ざってしまうので既存のファイルは全部削除した

### jekyllのひな形を作成して、ビルド、それをpush
[この通り](http://jekyllrb-ja.github.io/tutorials/using-jekyll-with-bundler/#bunbler%E3%81%AE%E5%88%9D%E6%9C%9F%E5%8C%96)にする  
既にディレクトリはあるので
```bash
bundle init
```
から最後までやった。
その後pushした。

## サイトを編集したい人がすること
### 準備
* まずは上記の[ローカルでビルドする環境を構築](#ローカルでビルドする環境を構築)をやる
* クローンしてきて
* [ローカルでサイトをサーブ](http://jekyllrb-ja.github.io/tutorials/using-jekyll-with-bundler/#%E3%82%B5%E3%82%A4%E3%83%88%E3%82%92%E3%82%B5%E3%83%BC%E3%83%96%E3%81%99%E3%82%8B)（ビルドしてローカルで表示できるようにする）してみる

### topページの編集
* [ここ](https://howpon.com/9443#Jekyll-3)の「タイトルや連絡先がデフォルトのままなので変更します。基本的な情報を変更するには「_config.yml」を修正します。」以下を参照

### 記事の追加

* [フォルダと役割](https://www.bluemoai.tech/article-7)に合わせて、公開する記事、作成中の記事、メモを置く

    * まずは「_drafts」でいろいろやってみる。このフォルダ内は公開されない。次のようにserveしたときだけ表示される。
    ```bash
    bundle exec jekyll serve --drafts
    ```
    ちなみに「2020-04-30-welcome-to-jekyll.markdown」がひな形なので参考になりそう
    * 公開するときは「_posts」に入れてpush