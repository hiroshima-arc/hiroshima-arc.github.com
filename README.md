サイトページ
===================

# 目的 #
MiddleManを使ってHiroshima-ARCサイトを管理する。

# 前提 #
| ソフトウェア   | バージョン   | 備考        |
|:---------------|:-------------|:------------|
| OS X           |10.8.5        |             |
| ruby           |2.2.1-p85    |             |
| rbenv          |0.4.0        |             |
| middleman      |3.2.0         |             |
| bootstrap      |3.0.2         |             |

+ GitHubにhiroshima-arc.ioが作成されている

# 構成 #
+ セットアップ

# 詳細 #

## セットアップ ##

    $ rbenv install 2.2.1
    $ rbenv global 2.2.1
    $ bundle
    $ git init
    $ git remote add origin git@github.com:hiroshima-arc/hiroshima-arc.github.com.git
    $ bundle exec middleman build
    $ bundle exec middleman deploy
    $ git add .
    $ git commit -a -m "セットアップ"
    $ git branch dev
    $ git checkout dev
    $ git push origin dev

# 参照 #

[Github Pages について整理しておきます](http://blog.eiel.info/blog/2013/02/17/github-pages/)

[middleman-blogをgithubでホストする](http://blog.coiney.com/2013/06/21/host-middleman-blog-on-github/)
