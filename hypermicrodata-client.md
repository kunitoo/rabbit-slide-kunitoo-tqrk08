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

Ruby Kaigi 参加しました?

# 今日話すこと

* Ruby Kaigi で感じたこと
* 試してみたこと

# 聞きましたか?

Hypermedia: The Missing Element to Building Adaptable Web APIs in Rails を聞いて感じたこと

# まだ見ていない方

http://rubykaigi.org/2014/presentation/S-ToruKawamura

# 自己紹介

* Kunihiko Ito
* @kunitoo

# Hypermedia: The Missing Element to Building Adaptable Web APIs in Rails の概要


# hypermicrodata とは

# 感じたこと

クライアントを作成することがとても難しそう...

# 利点

* 遷移先のurlを変更になってもクライアントを変更しなくてもよい

# 利用できそうなケース

* フローが変化しにくいもの

# ケース

ユーザー登録などの入力を繰替えすフローなど

# ユーザー登録のフロー

* ユーザー名
* アドレス
* URL
* 会社
* locaiton

# 画面設計

# どう使うの?


# user/1

$ curl -H "Accept: application/vnd.amundsen-uber+json" localhost:3000/users/1

