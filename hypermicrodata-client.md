# Hypermicrodata client

author
:   Kunihiko Ito

institution
:  永和システムマネジメント

presentation-date
:  2014/11/29

allotted-time
:  5m

# はじめに

Ruby Kaigi 2014 参加しました?

# 今日話すこと

* Ruby Kaigi 2014 で感じたこと
* 試してみたこと

# 参加しました?

Hypermedia: The Missing Element to Building Adaptable Web APIs in Rails

# 聞いていない方

* Video: http://rubykaigi.org/2014/presentation/S-ToruKawamura

# はじめまして

* 初参加
* Kunihiko Ito
* @kunitoo

# 概要

Hypermedia: The Missing Element to Building Adaptable Web APIs in Rails

* 疎結合なAPI
* 状態遷移をレスポンスに含める
* 設計
  * WEB API
  * HTML WEB アプリ

# hypermicrodata

* HTMLをJSONに変換
* HTMLから抽出
  * mirodata
  * リンク
  * フォーム

# あらためて

* Video: http://rubykaigi.org/2014/presentation/S-ToruKawamura

# 感じたこと

* サーバは簡単に作成できそう
* クライアント難しくなりそう

# 実際に作ってみよう！

* rails g scaffold User
  * name
  * email
* view に microdata を付加

# show.html.haml

    .person{itemscope: true, itemtype: 'http://schema.org/Person',
            itemid: users_url(@user), data: {main_item: true}}
      .media
        .media-body
      %p#notice= notice
      %p
        %strong Name:
        %span{itemprop: 'name'}= @user.name
      %p
        %strong Email:
        %span{itemprop: 'email'}= @user.email
      = link_to 'Edit', edit_user_path(@user), rel: 'edit'
      |
      \#{link_to 'Back', users_path, rel: 'collection', itemprop: 'isPartOf'}
{: lang="haml"}

# uber+json

    {
       "uber":{
          "version":"1.0",
          "data":[
             {
                "url":"http://localhost:3000/users.1",
                "name":"Person",
                "data":[
                   {
                      "name":"name",
                      "value":"Kunihiko Ito"
                   },
                   {
                      "name":"email",
                      "value":"kuni.110.92@gmail.com"
                   },
                   {
                      "name":"isPartOf",
                      "rel":"collection",
                      "url":"/users"
                   },
                   {
                      "rel":"edit",
                      "url":"/users/1/edit"
                   }
                ]
             }
          ]
       }
    }

# アイディア

クライアントが hypermicrodata と
同じルールで読みとれれば
簡単に作れるようになるのでは?

# やってみて

* microdata の付加が難しい
  * http://schema.org/
* メタ的に考える必要がある
* もっとデフォルトでできるとうれしい

# hypermicrodata client

みなさんも挑戦してみて下さい
