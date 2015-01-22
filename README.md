# [GeoNames.jp](http://geonames.jp/)

このレポジトリでは [GeoNames.jp](http://geonames.jp/) の仕様やドキュメント、リファレンス等を整理します。
技術情報を含む最新の情報については [Wiki](wiki) にて更新しています。


## Background
世界中の地名に対して URI を付与する基盤である [GeoNames.org](http://www.geonames.org/) は、LOD Cloud の中でも重要な地位を占めています(2014年時点で DBPedia に次ぐ第二位)。しかし、日本国内では GeoNames.org が積極的に活用されているとは言い難い状況です。われわれはこの原因を以下のように考えました。

* 日本地名の収録数が少ない（量の問題）
* データのミス・不整合がある（質の問題）
* 地名が日本語以外の言語で定義されており使いづらい（利用性の問題）

## Solution
GeoNames.org の日本版として [GeoNames.jp](http://geonames.jp/) を立ち上げました。

* 都道府県～町丁目にいたる地名を収録
* 日本語地名をそのまま使用できる簡便な URI 設計
* HTTP 仕様に忠実な API の提供 （リダイレクト、コンテントネゴシエーション）
* GeoNames.org のオントロジを使用した RDF の提供

## Application
以下のような分野への応用を期待しています。

* 統計分野：[e-Stat API](http://www.e-stat.go.jp/api/) から[Data Cube](http://www.w3.org/TR/vocab-data-cube/) を作成する際のエリア識別子として
* 機械学習：テキストマイニングによって抽出された地名に付与する識別子として
* 公共分野：[IMI 共通語彙](http://goikiban.ipa.go.jp/) における、地理識別子の選択肢のひとつとして

## ToDo
* 表記揺らぎ、不整合の解消（元データ作成機関へのフィードバックも含む）
* 過去地名、非公式地名など、収録範囲の拡大
* GIS コミュニティとの連携
* DBPedia 等の外部データセットと連携するためのリンクセットの充実


