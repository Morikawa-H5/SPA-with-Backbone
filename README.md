# Backbone.jsでSingle page アプリケーションを作る方法
### How to build single page application with Backbone.js

=================
## <a name='mokuji'>目次</a>
1. [はじめに](#intro)
1. [ワイアーフレーム](#wireframe)
1. [ページ構成](#pageStructure)
1. [View統治ポリシー](#viewManagePolicies)
1. [使用ライブラリ](#libs)
1. [ワイアーフレーム作成](#makeWireframe)
1. [イベント統治ポリシー](#eventManagePolicies)
1. [SearchBarからHistoryへのイベント伝播](#searchToHistory)
1. [HistoryからSearchResultへのイベント伝播](#historyToResult)
1. [SearchBarからSearchResultへのイベント伝播](#searchToResult)
1. [Tabから他のViewへのイベント伝播](#tabToOther)
1. [仕上げ](#finish)
1. [まとめ](#summary)
 
## <a name='intro'>はじめに</a>

Backbone.jsでアプリケーションを作成した際に、Viewが大きくなるという経験をしたことがある方も多いと思います。Viewが肥大化した場合、私達はViewをある単位の塊りで分割しようと試みるのですが、どのように分割するのが最善かという事は常に頭を悩ませるポイントです。

さらに、Viewを細かく分割した場合、それらをどのように結合してアプリケーションを作成するのが最善かという、新しい悩みも生まれます。

このチュートリアルでは、これらView分割に起因する問題についての私なりの最善策です。もちろんBackbone.jsでアプリケーションを作る方法は一つではありませし、View以外にまつわる問題が存在することも事実です。今回はそれら別の問題があることも認めつつ、Backbone.jsでアプリケーションを作る上で、まず最初に直面するView分割と結合に重点を置いて説明します。

## <a name='wireframe'>ワイアーフレーム</a>

作成するアプリケーションは幾つかのViewで構成されます。

* SearchBar：Webサービスに対してキーワード検索する。検索した場合、Historyに履歴が追加され、Resultsに結果が表示される。
* History：検索履歴。検索履歴をクリックすることで再検索することができる。
* Tab：Resultに表示する検索サービスを切り替えることができる。
* Result：検索結果を表示する。

ワイアーフレームのイメージは次の通りです。

<img src="./img/wireframe.png">

## <a name='pageStructure'>ページ構成</a>

### ページ構成

ページ構成は以下の通りです。


### 使用ライブラリ

以下のライブラリを使用しています。

* Backbone.js
* Underscore.js
* jQuery
* backbone.localStorage.js
* moment.js
* handlebars.js（任意）

デザインはBootstrapです。

####　補足

テンプレートエンジンにhandlebars.jsを利用しています。
こちらはUnderscore.jsのtemplateや他のテンプレートエンジンで代用することも可能です。

また、CSSプリプロセッサにStylusを利用していますが、この説明ではコンパイル後のピュアなCSSをベースに話を進めていきます。（とは言っても、CSSがメインテーマではないため、ほとんど話には登場しません。）

これらにはビルドプロセスが必須ですので、Gruntを使ってビルドしています。
Gruntの設定については詳しく説明しませんが、Gruntfile.jsはこちらを参照してください。

## <a name='viewManagePolicies'>View統治ポリシー</a>

## <a name='makeWireframe'>ワイアーフレーム作成</a>

## <a name='libs'>使用ライブラリ</a>

## <a name='eventManagePolicies'>イベント統治ポリシー</a>

## <a name='searchToHistory'>SearchBarからHistoryへのイベント伝播</a>

## <a name='historyToResult'>HistoryからSearchResultへのイベント伝播</a>

## <a name='searchToResult'>SearchBarからSearchResultへのイベント伝播</a>

## <a name='tabToOther'>Tabから他のViewへのイベント伝播</a>

## <a name='finish'>仕上げ</a>

## <a name='summary'>まとめ</a>
