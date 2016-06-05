サイトページ
===================

# 目的 #
MiddleManを使ってHiroshima-ARCサイトを管理する。

# 前提 #
| ソフトウェア   | バージョン   | 備考        |
|:---------------|:-------------|:------------|
| vagrant        |1.7.4        |             |
| ruby           |2.3.0        |             |
| rbenv          |0.4.0        |             |
| middleman      |3.2.0         |             |
| bootstrap      |3.0.2         |             |

+ GitHubにhiroshima-arc.ioが作成されている

# 構成 #
+ セットアップ

# 詳細 #

## セットアップ(動作確認)
    $ vagrant up
    $ vagrant ssh
    $ git clone -b dev https://github.com/hiroshima-arc/hiroshima-arc.github.com.git
    $ cd hiroshima-arc.github.com/
    $ bundle install --path ./vendor/bundle
    $ bundle exec middleman
    
ローカルマシンから`http://localhost:8080/`で動作を確認する。    

## セットアップ(デプロイ)
    
    $ git checkout dev
    $ bundle exec middleman build
    $ bundle exec middleman deploy
    $ git add .
    $ git commit -a -m "コメント"
    $ git push origin dev

## Rakeコマンド

    $ bundle exec rake -T
    rake build      # Build Blog
    rake deploy     # Deploy website
    rake go[msg]    # One Line deploy
    rake push[msg]  # Commit and push changes to Github


# 参照 #

+ [Github Pages について整理しておきます](http://blog.eiel.info/blog/2013/02/17/github-pages/)
+ [middleman-blogをgithubでホストする](http://blog.coiney.com/2013/06/21/host-middleman-blog-on-github/)
+ [A Custom Rakefile for One Line Middleman Deploy](http://www.colbycheeze.com/blog/2015/03/a-custom-rakefile-for-one-line-middleman-deploy.html)
