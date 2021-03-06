---
title: ブラウザでVS Codeが使える！「Coder」を試してみる
description: |-
  VS Codeが使えるクラウドIDE「Coder」を試してみます
  導入→プロジェクト作成→GitHubからソース取得→開発サーバー起動→画面表示確認まで行います
date: 2019-03-04T11:11:49.097Z
image: /images/uploads/coder22.png
categories:
  - 使ってみるシリーズ
tags:
  - 使ってみるシリーズ
  - Coder
comments: true
---
## はじめに
私は普段の業務でもプライベートの開発でも<a href="https://code.visualstudio.com/">Visual Studio Code(VS Code)</a>を使っています。<br>
朝の時間が一番集中できるので、朝早起きして開発をしたりもするのですが、１ヶ月ほど前、出社が遅いことを上司に指摘されたため、しぶしぶ早めに朝出社することにしたのですが、中途半端に作業に切りをつけるのが嫌で、いっそのことめちゃくちゃ早く出社して開発しようと思いました。<br>

そこで問題となったのが自宅と同等の開発環境を職場のPCにも用意する必要があるということなのですが、構築もめんどくさいですし、むやみに色々入れるとそれはそれで何か言われそうなので、どうしたものかなーって思っていました。

そこで白羽の矢を立ったのがクラウドIDEで、その時は<a href="https://codeanywhere.com/">Codeanywhere</a>というクラウドIDEで、１週間ほど使っていたのですが、やはりVS Codeとの違いが気になり、そのうち使わなくなってしまいました。<br>
その後は朝の時間は読書にあてていて、それはそれで捗ったのですが、Coopet(私が開発しているSNS)の開発も考えると、朝の時間をコーディングにあてたいと思うようになりました。<br>
そこで少し調べてみたところ、<a href="https://coder.com/">Coder</a>を見つけたという流れです。<br>

今日は使ってみるシリーズ第4弾ということで(Elmは勉強中です)、クラウドIDE「Coder」を使ってみようと思います。<br>

## クラウドIDEとは

そもそもクラウドIDEとは何かというところから、お話したいと思います。<br>
クラウドIDEはその名の通り、「<span class="strong-str">クラウド上に構築されたブラウザからアクセスできる開発環境</span>」を指します。<br>
普段皆さんが開発する時はもちろん皆さん自身のパソコンの中にパッケージ管理ツールを入れたり、エディタを入れたり、データベースサーバーを立てたりして、開発環境を構築すると思います。<br>
クラウドIDEではそういった環境構築を、皆さんのパソコンの中でするのではなく、クラウド上で行い、そして皆さんのパソコンからブラウザを通して、クラウド上の開発環境にアクセスすることになります。<br>

クラウドIDEには以下のようなメリットがあります。<br>

・開発環境のプリセットが用意されており、それを選ぶだけで容易に開発環境を構築できる<br>

・ソースのビルドやサーバーの起動は自分のパソコンでなく、クラウド上で行われるため、自分のパソコンのリソースの消費を抑えて開発が可能。<br>

・開発端末が変わっても環境構築をやり直す必要がない

特に1点目は初学者の1つ目の壁である環境構築を格段にやりやすくしてくれる点なので、クラウドIDEは初学者にもおすすめのサービスとなっています。<br>

## Coderとは

<a href="https://coder.com/">Coder</a>は端的に言えば「(ほぼ)VS Codeが使えるクラウドIDEサービス」です。現在はアルファ版として公開されています。<br>
実はVS CodeライクなクラウドIDEは他にもあるのですが、Coderが優れているのは、<span class="strong-str">大半のVS Code拡張機能が使用できる</span>点にあります。<br>
<img src="/images/uploads/coder.png" style="width: 100%;"/>

言語サポートはこんな感じになっています。<br>
<img src="/images/uploads/coder2.png" style="width: 100%;"/>

よく目にするようなものは揃っている印象ですね。<br>
とりあえず私の用途では困らなさそうです。<br>
プロジェクトはDockerコンテナ内に作成されるので、ある程度融通も効きそうですしね。<br>
バージョンもボタン一つで切り替えられるとのこと<br>

また、「Fast Time」という機能を使うと時間制ですが、96CPUコア(!)、メモリ16GBが利用可能になるとのこと。<br>
今回は使いませんが、重いビルドなどするときには試してみたいですね。

## 登録してみる

それでは早速使ってみましょう。<br>

<a href="https://coder.com/">公式ページ</a>にアクセスします。<br>

<img src="/images/uploads/Coder3.png" style="width: 100%;"/>

サインアップにはGithub、Google、Emailが選べるみたいですね。<br>
今回はGithubでサインアップしようと思います。<br>

<img src="/images/uploads/Coder4.png" style="width: 100%;"/>

ログインを求められるので、ユーザー情報を入力してログインします。<br>

<img src="/images/uploads/Coder5.png" style="width: 100%;"/>

するとCoderとGitHub連携の認証を求められるので「Authorize codercom」をクリックして認証します。<br>

<img src="/images/uploads/Coder6.png" style="width: 100%;"/>

認証が完了するとCoder側に戻ってきて、ユーザー名と電話番号の入力を求められます。<br>
SMS認証が必要なのは予想外でした。<br>
複数アカウント防止用でしょうか。<br>
入力して「Complete Sign Up」をクリックします。<br>
<img src="/images/uploads/Coder7.png" style="width: 100%;"/>

これにて登録完了です！<br>

## 使ってみる

### プロジェクトを作成する

<img src="/images/uploads/Coder7.png" style="width: 100%;"/>

まずはプロジェクトを作成してみましょう。<br>
左上にある「+ Create Project」をクリックします。<br>
するとプロジェクト名の入力を求められるので、入力します。<br>
私は「Coopet」と入力しました。<br>
<img src="/images/uploads/Coder8.png" style="width: 100%;"/>

するとプロジェクト行が追加されるので、「Open in VSCode」をクリックします。<br>

すると...<br>
<img src="/images/uploads/Coder9.png" style="width: 100%;"/>

おおー！<br>
これはまさにVS Code!<br>
ここまで再現されているとは...<br>

「Ctrl+@」でターミナルもちゃんと開きます。<br>

<img src="/images/uploads/Coder10.png" style="width: 100%;"/>

Emmetも...

<img src="/images/uploads/Coder11.png" style="width: 100%;"/>

<img src="/images/uploads/Coder12.png" style="width: 100%;"/>
使えますね！

### GitHubからソースコードを取得する

さて、それではGitHubで管理しているCoopetのソースコードを取得してみましょう。<br>
現状GUIで取得する機能はないようで、統合ターミナルにコマンドを入力して取得します。<br>
以下のコマンドを発行して取得しました。<br>

```
git init
git remote add origin https://github.com/RinGoku/coopet.git
git fetch origin
git merge origin/development
```

<img src="/images/uploads/Coder13.png" style="width: 100%;"/>

無事取得できました！
次にnpmで関連パッケージをインストールします。<br>
そのままですと、npmコマンドが使えないので、Node.js環境を使えるようにします。<br>
「Ctrl+Shift+P」を押下して、コマンド入力バーを開き、「mount」と入力すると「Mount Volume」が候補に出てくるので選択します。<br>

<img src="/images/uploads/Coder14.png" style="width: 100%;"/>

するとマウント可能な一覧が表示されます。<br>

<img src="/images/uploads/Coder15.png" style="width: 100%;"/>

JavaやGoの姿も見えますね。<br>
今回はnode/11.0.0を選びました。<br>

これでnpmコマンドが使えるようになるので、早速npm installすると...<br>

<img src="/images/uploads/Coder16.png" style="width: 100%;"/>

インストール完了ですね！

それでは、ionic serveコマンドでサーバーを起動してみます。<br>
(Ionicコマンドを使えるようにするために、「npm i ionic -g」を実行しました)

<img src="/images/uploads/Coder17.png" style="width: 100%;"/>

起動しましたね。<br>
しかしこのままでは私の端末から、このCoder上のサーバーには接続できません。<br>
この開発環境の「localhost」に外部からアクセスすることができないからです<br>

なので「ngrok」というサービスを使用します。<br>
簡単に言えば、ローカルPC上(localhost)で稼働しているネットワークサービスを外部に公開できるサービスです。<br>
今回はこのCoder環境に導入することで、私の端末からアクセスできるようにします。<br>
以下のコマンドを実行します。<br>

```
npm install serve ngrok
npx ngrok http 8100
```

成功すればこんな感じの画面が表示されます。
<img src="/images/uploads/Coder18.png" style="width: 100%;"/>

この「http://269f45fa.ngrok.io 」というURLにアクセスすると、このCoder上の「http://localhost:8100 」にアクセスしたことと同義になります(URLはngrokの実行ごとに変わります)。<br>

さて早速アクセスしてみましょう...といいたいところですが、この方法でアクセスするためには起動コマンドを以下のように変える必要があります。<br>

```
ionic serve -- --disable-host-check
```

詳しくは説明しませんが、このオプションを付けないと、真っ白な画面に「Invalid Host header」という文字が表示されるだけで、実際のアプリケーションを表示することができません。<br>
この起動コマンドでサーバーを起動し、「http://269f45fa.ngrok.io 」にアクセスしてみると...
<img src="/images/uploads/Coder19.png" style="width: 100%;"/>

やりました！

## おわりに

今回はクラウドIDE「Coder」を使ってみる過程を解説しました。<br>

正直、ブラウザ上でいじっていることを忘れるくらいにはVS Codeそのものなので、Codeanywhereで感じていた違和感がかなり払拭できそうです。<br>

さらっと流しましたが、「ngrok」もなかなかすごいサービスですので、皆さん使ってみてください。<br>

まだCoderの肝となる拡張機能に関しては試せていないので、実際に開発した使用感も含めて、また記事にできたらなと思います。<br>

それでは今回はこの辺で。ここまで読んでいただきありがとうございました！

感想やご意見・質問等ございましたら、<a href="https://twitter.com/RinGoku98">私のTwitter</a>までお気軽にどうぞ。
