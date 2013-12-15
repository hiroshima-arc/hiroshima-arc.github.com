サイトページ
===================

# 目的 #
MiddleManを使ってHiroshima-ARCサイトを管理する。

# 前提 #
| ソフトウェア   | バージョン   | 備考        |
|:---------------|:-------------|:------------|
| OS X           |10.8.5        |             |
| ruby           |2.0.0-p247    |             |
| rvm            |1.24.0        |             |
| middleman      |3.2.0         |             |
| bootstrap      |3.0.2         |             |

+ GitHubにhiroshima-arc.ioが作成されている

# 構成 #
+ セットアップ

# 詳細 #

## セットアップ ##

    $ rvm use ruby-2.0.0-p247
    $ rvm gemset create hiroshima_arc_githubpage
    $ rvm use ruby-2.0.0-p247@hiroshima_arc_githubpage
    $ bundle
    $ git init
    $ git remote add origin git@github.com:hiroshima-arc/hiroshima-arc.github.com.git
    $ bundle exec middleman build
    $ bundle exec middleman deploy

# 参照 #

[Github Pages について整理しておきます](http://blog.eiel.info/blog/2013/02/17/github-pages/)

[middleman-blogをgithubでホストする](http://blog.coiney.com/2013/06/21/host-middleman-blog-on-github/)
