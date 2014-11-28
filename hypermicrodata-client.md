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

# アイディア

クライアントが hypermicrodata と
同じルールで読みとれれば
簡単に作れるようになるのでは?

# 実際に作ってみよう！

* rails g scaffold User
  * name
  * email
* view に microdata を付加

# client

* 

# やってみて

* microdata の付加が難しい
  * http://schema.org/

