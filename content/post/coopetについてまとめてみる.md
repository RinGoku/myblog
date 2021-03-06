---
title: Coopetについてまとめてみる
description: |-
  私が開発しているSNS「Coopet」についてまとめてみました。
  概要や採用技術の紹介を行います。
date: 2019-03-05T11:24:14.691Z
image: /images/uploads/twitter_header_photo_1.png
categories:
  - Coopet開発
tags:
  - Coopet開発
comments: true
---
## はじめに

今回の記事は私が開発しているSNS、「Coopet」について説明してみるというものです。<br>
完成したサービスの紹介でなく、まだまだ企画段階なのですが、現時点で考えていることについてまとめておこうと思います。<br>
いつもの記事のような技術解説的な要素は薄めなのですが、よろしければ御覧ください！

<script async src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script><ins class="adsbygoogle" style="display:block; text-align:center;" data-ad-layout="in-article" data-ad-format="fluid" data-ad-client="ca-pub-9721752780042654" data-ad-slot="5186585524"></ins><script>(adsbygoogle = window.adsbygoogle || []).push({});</script>

## Coopetとは

<img src="/images/uploads/twitter_header_photo_1.png" style="width:100%;"/>

Coopetは「ペットでつながるSNS」をテーマにしたサービスです。<br>

以下のような機能の搭載を予定しています。<br>
・Twitter的なつぶやき機能(ペット画像・動画投稿、いいね・コメント機能)<br>
・ペット管理機能（餌やり、散歩記録）<br>
・ペットプロフィール機能(どんな動物か、可愛いのかかっこいいのかなどをタグ付けして検索できるような)<br>

まだランディングページとログイン画面しか作ってないですが、こんな感じの画面になる予定です。<br>

<section style="display:flex;align-items: flex-start;
">
<img src="/images/uploads/coopet1.png" style="width:50%;"/>
<img src="/images/uploads/cooprt2.png" style="width:50%;"/>
</section>

目標としてはフリーランスとして活動を始める、8月までにはなんとかオープンしたいと思っています。<br>

## なぜ作ろうと思ったのか

SNS的なWebサービスを作ろうと思ったのは、８月からフリーランスとして活動するにあたり、人に見せられるポートフォリオ的なものがほしいと思ったからですね。<br>

現在はSIerとしてお客さんが業務で使用するWebアプリケーションを開発しているのですが、そうしたアプリケーションはオープンなWebサービスではなく、お客さんのイントラネット内でしか使用できないものだったりするので、他の人にこんなもの作りましたーって実物を見せることができないんですね。<br>
業務経歴書で説明すればいいんですが、やはり目で見てもらうのが一番わかりやすいですし、説得力もあるのかなーと。<br>

その中でも「ペットでつながるSNS」というテーマを掲げたのは、私自身ペットを飼っており、動物好きであるからですね。<br>
(私が飼っているのはデグーマウスという動物です！興味のある方はぜひYoutubeなどで調べてみてください！)

やろうとしていることは大体Twitterみたいなものなんですが、Twitterは世界中の人が色々なことを呟いているので、その中からペットや動物関連の話題だけを集めるのも大変ですし、ペットや動物関連の発信をしても他の話題に埋もれてしまうことも多いと思います。<br>

ですので、ペットを中心としたSNSを作れば、自分のペットの可愛さを発信したい人や、動物を見て癒やされたい人には話題が絞れていいんじゃないかと思ったんです。<br>

## 技術構成は？

Coopetは以下のような構成で作ろうと思っています。<br>

<img src="/images/uploads/coopet_structure.png" style="width:100%;"/>
各々軽く解説していきます。<br>

### フロントエンド

#### Angular

<img src="/images/uploads/angular.png" />

フロントエンドのJavaScriptフレームワークは自分が最も使い慣れている「Angular」を使用します。<br>
Webエンジニアとして自分の最も売りとなると考えている部分はこのAngularの業務経験だと思っているので、そこをアピールするためにもここは外せません。<br>

#### Ionic

<img src="/images/uploads/ionic-framework-og.png" style="width:100%;"/>

Angularと相性の良いUIフレームワークということで選定しました。<br>
また今回のアプリはPWAとして開発したいと思っているので、それに標準対応している部分も評価しました。<br>
詳しい選定内容については<a href="https://elated-blackwell-51e103.netlify.com/post/2019%E5%B9%B4%E3%81%AB%E9%81%B8%E3%81%B6%E3%81%B9%E3%81%8D%E3%83%A2%E3%83%90%E3%82%A4%E3%83%ABui%E3%83%95%E3%83%AC%E3%83%BC%E3%83%A0%E3%83%AF%E3%83%BC%E3%82%AF%E3%81%AF/">こちらの記事</a>をご覧ください。<br>

### サーバーサイド

<img src="/images/uploads/aws.png" style="width:100%;"/>

サーバーサイドは基本、AWS(Amazon Web Service)を使おうと思っています。<br>
自分が持っている技術をアピールするという観点で考えると、実務経験のないAWSを選定しているのはAngularの選定理由と矛盾しますが、私はバックエンド側の経験はそれほどなく(Javaでひと通りはやっていますが)、
またシングルページアプリケーションにするとサーバーサイドはかなり薄くなるので、Javaフレームワークでごりごり書くよりは、パブリッククラウドのサービスを組み合わせてコード量も最小限に抑えようと考えました。<br>
パブリッククラウドは今後避けては通れないところだと思っているので、今のうちに触っておきたいというのも理由のひとつですね。<br>
パブリッククラウドの中でもAzureやGCPでなくAWSを選んだのは、単純にネット上に情報量が多いという点からですね。<br>
後聞くところによるとサポートも迅速で質も高いらしいので、パブリッククラウド初心者には優しいのかなと。<br>

使用するAWSの各サービスについては詳細はまた記事にしてご紹介しようとも考えているので、ここでは最小限の紹介で済ませます。<br>

・AWS Cognito(ユーザーのサインアップ/サインインおよびアクセスコントロール)<br>
・Amazon API Gateway(Web API の作成)<br>
・AWS Lambda (サーバー側業務ロジック) <br>
・Amazon S3(動画像の保存)<br>

## おわりに

今回は私が開発しているSNSサービス「Coopet」をご紹介しました。<br>
本業とゲーム開発の合間を縫って開発することになるので、そこまで多くの時間リソースを割けないのですが、少しずつ形にしていきたいと思います。<br>
進捗状況はこのブログの記事や私のTwitterでお伝えしていこうと思います。<br>
それでは今回はこのへんで。ここまで読んでいただきありがとうございました！

感想やご意見・質問等ございましたら、<a href="https://twitter.com/RinGoku98">私のTwitter</a>までお気軽にどうぞ。
