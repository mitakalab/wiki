## Macの環境構築

ここでは、Mitakalabで開発を行なっていくにあたり、そのための環境構築を説明していきます。


## XcodeとCommand Line Toolsのインストール

Macで開発を行なっていくにあたり、Xcodeのインストールは必須です。
iOSやOS Xのアプリを作る用途以外に必要なコンパイラがXcodeに入っているので、まずはXcodeをインストールしましょう。

Xcodeのインストール辞退はApp Storeで配布されているので、そこからダウンロードしてインストールします。

Xcodeのインストールが終わったら、 Command Line Toolsのインストールを行います。

これは、あとで行うHomebrewのインストールの際に必要になってきます。

![](http://media.tumblr.com/ca0a3c39c11120ca412bead585c494f0/tumblr_inline_mp32dcEY661rbxx4s.png)

Command Line ToolsはXcodeを開き、上のメニューのPreferences > DownloadsからCommand Line Toolsをインストールします。

iPhoneやiPadのアプリを開発する上で、iOSシミュレーターが必要になるので、一緒にダウンロードしましょう。


Xcodeの参考URL

- [Wikipedia : Xcode](http://ja.wikipedia.org/wiki/Xcode)




## Homebrewのインストール

Homebrewはいわゆるパッケージ管理システムといわれるもので、Macでこれから必要なものを依存関係などを含めカンタンにインストールすることができるものです。

Homebrewさえ入れば、あとは必要な物はHomebrewを使ってインストールすることができます。

Command Line Toolsのインストールが終わったら、homebrewをインストールしましょう。

Terminalを開いて

    ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"


と入力すれば、Homebrewが入ります。

![](http://media.tumblr.com/7705e46f9104bdad7d27aa240b0ae991/tumblr_inline_mp32x4D1yp1rbxx4s.png)


Homebrewの参考URL

- [GitHub : mxcl/homebrew](https://github.com/mxcl/homebrew)
- [Homebrew : Homebrewの公式サイト](http://mxcl.github.io/homebrew/)




## Gitのインストール

GitはLinuxの開発者Linus Torvaldsが作った、コードのバージョン管理システムで、これも開発を進めていく上で必須のツールになります。

特に、Mitakalabでは[GitHub](https://github.com)の使用を推奨しているので、そのためにも必要になってきます。

GitはHomebrewを使えばカンタンにインストール出来ます。

Terminalで同様に

    brew install git

とすれば、カンタンにGitをインストールすることができます。

Gitの参考URL

- [Wikipedia : Git](http://ja.wikipedia.org/wiki/Git)
- [GitHub : git/git](https://github.com/git/git)
- [Git : Gitの公式サイト](http://git-scm.com/book/ja/)
- [GitHub - Build Software Better, Together](http://github.com)
- [Code School Try Git : GitHubが提供しているGitをWeb上で学べるサイト](http://try.github.io/levels/1/challenges/1)



## Oh-my-zshのインストール

開発を進めていく中で、Terminalはもっともよく使うツールです。  

そのTerminalを使うにあたって、Shellというものを理解しましょう。

Shellという名前は、貝殻のシェルからとられていて、OSの核となるKernelとユーザーとの間にあるものというところからシェルという名前がつきました。

カンタンに言えば、Shellはユーザー（Terminalで入力したコマンドなど）とOSのKernel（そのコマンドをマシンとして実行するなど）とをつなぐ役割を担っています。

多くのUNIX系マシンでは標準でbash（Bourne Again SHellの略です）が採用されています。


しかし、Mitakalabではbashよりも機能が豊富なzshを採用しています。

そこで、ここではzshの便利なツールをまとめてあるoh-my-zshをインストールします。

Terminalで

    curl -L https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh | sh

とすれば、oh-my-zshがインストールされます。

![](http://media.tumblr.com/598fc1074a9a1b38c75d878e57677ed7/tumblr_inline_mp3el1Cob31rbxx4s.png)

一度Terminalを閉じて再度開くと、このように色がついてみやすくなったり、自動補完機能がつくようになっているのがわかると思います。

![](http://media.tumblr.com/e592f09fdedc40a36998ef52e2e2d0f5/tumblr_inline_mp39rzSfUP1rbxx4s.png)

Terminalの色はメニューのPreferencesから変更することができます。

またオプションとして、Terminalより機能の豊富なiTermを使いたい場合は、[iTermのサイト](http://www.iterm2.com/#/section/home)からダウンロードして使うことができます。

![](http://media.tumblr.com/310e99797ea7610faee730f00ebdd340/tumblr_inline_mp39ylBWih1rbxx4s.png)

Oh-my-zshの参考URL

- [Wikipedia : シェル](http://ja.wikipedia.org/wiki/シェル)
- [Wikipedia : Bash](http://ja.wikipedia.org/wiki/Bash)
- [Wikipedia : Zsh](http://ja.wikipedia.org/wiki/Zsh)



## EmacsとSublimeTextのインストール

プログラミングを行う上で、最も重要なツールはエディタです。
なぜなら、プログラミングはコードを書くことが全てなので、そのコードをいかに効率良く書けるかは、エディタによって変わってくるからです。

エディタが優れていれば、人の何倍も生産性を高めることができるといっても過言ではありません。

MitakalabではエディタとしてEmacsとSublimeTextを推奨しています。

EmacsはRubyを開発したMatzことまつもとひろゆきさんや、Facebookを作ったMark Zuckerbergなど、数えきれないほどの優れたハッカーが愛用するエディタです。

SublimeTextは近年、非常に人気を集めているエディタで、非常に優れているのでSublimeTextも合わせてインストールします。

> **注** Emacsを選択肢している理由は、はあくまでMitakalabで開発環境を共通化させ、開発を進めることに力を集中させるためです。
> また、EmacsのCtrlを多用したコマンドはMacのキーバインディングとして採用されている点も踏まえて、Emacsを推奨しています。
> Vimをきらっているわけではありません。
> Vimは本当に素晴らしいエディタです。


EmacsはHomebrewでインストールすることができます。

    brew install emacs

これで、最新版のEmacs 24.xがインストールされます。

ただし、このままでは、デフォルトで入っているEmacsが起動してしまうので、ZshにHomebrewでインストールしたEmacsを使うようにエイリアスを追加します。

    echo 'alias emacs="$(brew --prefix emacs)/bin/emacs"' >> ~/.zshrc

~/.zshrcを読み込みます。

    source ~/.zshrc

ここまでで、Emacsのインストールが完了です。
Terminalでemacsと打つと、次のような形でTerminal上でemacsが立ち上がるのがわかると思います。

![](http://media.tumblr.com/a3e5fe59423321554a78e02ac97bb4f7/tumblr_inline_mp3a0sUz561rbxx4s.png)

エディタを終了するには、Ctrl + Xと押したあとに、Ctrl + Cを押して閉じることができます。

（Emacsのプラグインの設定に関しては、別途また説明します。）



次に、SublimeTextをインストールします。

SublimeTextは[ここ](http://www.sublimetext.com)からカンタンにダウンロードすることができます。

SublimeTextは非常に豊富な機能があり、自分でも様々にカスタマイズできます。

SublimeTextは基本的に無料で使い続けることができます。


Emacsに関しては、はじめコマンドに慣れる必要があるので、以下の参考URL
などを参考にして、学んでみることをおすすめします。


参考URL

- [Wikipedia : Emacs](http://ja.wikipedia.org/wiki/Emacs)
- [ドットインストール : Emacs入門](http://dotinstall.com/lessons/basic_emacs)
- [ドットインストール : Sublimet Text 2入門](http://dotinstall.com/lessons/basic_sublimetext)



## Rubyのインストール

Macには標準で、Rubyがインストールされています。

Terminalを開いて、次のようにirbと入力するとRubyを対話型形式で試して見ることができます。

    irb(main):001:0> 1 + 1
    => 2

しかし、TerminalでRubyのバージョンを確認してみると、

    ruby -v
    > ruby 1.8.7 (2012-02-08 patchlevel 358) [universal-darwin12.0]

と古いバージョンが入っています。

RubyはHomebrewで最新版をインストールすることもできますが、その場合新しいバージョンをインストールすると、古いバージョンが上書きされてしまいます。

開発していくにあたり、Rubyのバージョンを共存させ、カンタンにバージョンを変更できれば、非常に便利になります。

rbenvはそのためのツールとして、最も人気のあるRubyのバージョン管理システムです。        

ここでは、rbenvを使ってRubyをインストールしましょう。

Terminalを開いて、まずはrbenvをインストールします。

    brew install rbenv  

インストールが完了したら、rbenvの設定をShellに追加します。ここではZshを使っているので、Zshの設定ファイルである、.zshrcに設定を追加します。

同じくTerminalで次のように入力します。

    echo 'eval "$(rbenv init -)"' >> ~/.zshrc

.zshrcを書き換えたら、その設定を読み込みます。

    source ~/.zshrc


次に、Rubyのビルドツールである、ruby-buildをインストールします。

    brew install ruby-build

そして、rbenvでRubyをインストールするために必要なrbenv-vars、openssl、readlineをそれぞれインストールします。

    brew install rbenv-vars openssl readline

ここまでで、rbenvを使う準備が整いました。


それでは、rbenvを使ってruby 1.9.3-p429をインストールします。

    rbenv install 1.9.3-p429

rbenv installコマンドでバージョンを指定してインストールできます。
Rubyのインストールには少し時間がかかります。

インストールが終わったら、今インストールした

    rbenv global 1.9.3-p429
    rbenv rehash

globalでシステム全体でこのバージョンを使用するように設定し、rehashで設定を反映します。

Terminalを再起動させ、Rubyのバージョンが変わっているかどうか確認してみましょう。

    ruby -v
    > ruby 1.9.3p429 (2013-05-15 revision 40747) [x86_64-darwin12.4.1]  


参考URL

- [Wikipedia : Ruby](http://ja.wikipedia.org/wiki/Ruby)
- [Ruby : Rubyの公式サイト](http://www.ruby-lang.org/ja)


## Ruby on Railsのインストール

Webアプリケーションを作ることが出来れば、非常にできることの範囲が広がります。

たとえば、iOSアプリやAndroidアプリの裏側にはWebアプリケーションがありますし、Arduinoと通信させることでハードウェアを操作させることもできます。TwitterやFacebookと連動しデータを可視化するものから、音声認識を使ったリモコンまでありとあらゆるものの土台にWebアプリケーションがあります。


Webアプリケーション自体は、ほぼあらゆる言語で開発することができます。

しかし、プログラミング言語自体はWebアプリケーションだけを作るために設計されているわけではないので、効率がわるい点があります。


そこで、Webアプリケーションを開発するために設計されたものをWebアプリケーションフレームワーク、通称フレームワークと言います。


フレームワーク自体はプログラミング言語ではありません。フレームワークはある特定のことに特化した機能を集めたものです。




MitakalabではWeb開発フレームワークとして、Ruby on Railsを推奨しています。

その理由は、最も先進的で安定しており、豊富なRubyGemsライブラリがあることで他のフレームワークに比べプロトタイプを作るスピードを早めることができるためです。

また、導入事例としては、[Twitter](https://twitter.com)、[Github](https://github.com)、国内だと[CookPad](http://cookpad.com)など非常にたくさんの導入事例があり、シリコンバレーのスタートアップでも過半数以上がRailsをはじめとした、Rubyフレームワークを使っているとも言われています。

また、Ruby自体たいへん素晴らしい言語であり、Rubyを使うことでプログラミングの理解を早く進められることができる点も、ひとつの理由です。

> **注** その他、後に紹介するJavaScriptのフレームワークであるNode.jsをはじめ、PythonのフレームワークであるDjangoやPHPのフレームワークであるCakePHPやFuelPHPなどもあります。
> それぞれメリットがあり、たとえばPythonは数値計算などのライブラリが優れているので、そうした場合には必要に応じて選ぶとよいと思います。
> またほとんどのフレームワークは、Ruby on Railsを参考にして作られているので、Railsを学べば基本的な部分はほとんど同じなので、問題なく他のものを使いはじめることができます。


RailsはRubyが提供しているライブラリであるRubyGemsのいちライブラリとして提供されています。

先ほど言ったように、フレームワークはプログラミング言語の一部であるので、ふつうのライブラリをインストールするのと同じように導入されます。


> **注** RubyGemsはRubyの公式ライブラリです。
> 6万個近くのライブラリが公開されています。

Terminalでインストールします。

    gem install rails

これで、Railsの現在の最新バージョンであるrails-4.0.0がインストールされたと思います。


参考URL

- [Wikipedia : RubyGems](http://ja.wikipedia.org/wiki/RubyGems)
- [Wikipedia : Ruby on Rails](http://ja.wikipedia.org/wiki/Ruby_on_Rails)
- [GitHub : rails/rails](https://github.com/rails/rails)
- [RubyGems : RubyGemsの公式サイト](http://rubygems.org)
- [The Ruby Toolbox : Gemをカテゴリーごとに探せるサイト](https://www.ruby-toolbox.com)
- [Ruby on Rails : Ruby on Railsの公式サイト](http://rubyonrails.org)
- [Railscasts : Railsを使ったアプリケーションの作り方を学べるサイト](http://railscasts.com)



## Node.jsのインストール

世の中にはたくさんの言語があります。なかでも、JavaScriptはダントツでもっとも広く使われている言語といっても過言ではありません。

> **注** GitHubの[言語ごとの順位](https://github.com/languages)を見るとわかります。


もともと、JavaScriptはブラウザ上でアニメーションをしたり、Google Mapsで広く知られたAjax（ページを再読み込みしないで表示だけが変わる技術）を行う用途で広く使われていました。

このような用途はクライアントサイドと呼ばれ、カンタンにいうとユーザーのブラウザ上だけで完結するものとしてのみ使われていました。

しかし、近年JavaScriptをもっとRubyやPythonのようにサーバーサイドでも使おうという動きが活発になり、そのフレームワークとしてNode.jsが開発されました。


Node.jsを直接使わないにしても、JavaScriptをターミナル上で動かすためにもNode.jsは非常に便利なので、ここでインストールします。


Rubyと同じようにHomebrewでインストールできますが、Node.jsのバージョン管理システムである、nodebrewを使えばrbenvと同じようにバージョンを共存させることができるので、それを使ってインストールします。


Terminalで

    curl https://raw.github.com/hokaccha/nodebrew/master/nodebrew | perl - setup

とすればnodebrewがインストールされます。

nodebrewを有効にするために、rbenvの時と同じように.zshrcに設定を追加します。

    echo 'export PATH=$HOME/.nodebrew/current/bin:$PATH' >> ~/.zshrc

そして.zshrcの変更を反映させます。

    source ~/.zshrc

これで、nodebrewを使う準備が整いました。

現在の最新安定版のv0.10をインストールします。同じくTerminalで

    nodebrew install v0.10

インストールが完了したら、それを設定します。

    nodebrew use v0.10

無事に設定されれば、バージョンを確認すると現在の最新である、v0.10.12となっていることが確認できます。

    node -v
    > v0.10.12

また、nodebrewでインストールしたnodeのバージョンも次のようにして確認できます。

    nodebrew ls

これで、Terminal上でJavaScriptを動かせるようになりました。

Terminalでnodeと入力すると

    node 
    > 1 + 1
    2

のような形で、JavaScriptを試すことができます。



## ExpressとCoffeeScriptのインストール


RubyのRubyGemsに当たるものが、JavaScriptではNode Packaged Modulesです。

このNode Packaged Modulesを使って、RubyのRuby on Railsにあたる、ExpressとCoffeeScriptをインストールします。

まずは、Expressをインストールします。

    npm intall -g express

この-gというのは、グローバルすなわちシステム全体にインストールする場合につけます。（もしもつけない場合は、現在のディレクトリのしたにインストールされてしまいます。）  



次に、CoffeeScriptをインストールします。

CoffeeScriptについて、少し説明すると、基本的にCoffeeScriptはJavaScriptと全く同じ言語だと考えてもらって大丈夫です。

ただ、JavaScriptは少し変わった文法で書きづらい側面があり、それを読みやすく書きやすくしたのがCoffeeScriptです。

なので、ただ見た目だけが違っているだけで、JavaScriptと全く同じ文法で、全く同じ挙動をします。


イメージとしては、JavaScriptもCoffeeScriptも同じ日本語だが、ちょっと現代人にとっては読みにくい古文に当たるものがJavaScriptで、読みやすく書きやすい現代文に当たるものがCoffeeScriptだと思っておけばいいと思います。

> **注** 実際CoffeeScriptは新しい言語で2009年の終わりにJavaScriptをもっと書きやすくするという目的で開発されました。
> しかし、今では非常に広く使われており、RailsでもJavaScriptではなくCoffeeScriptがデフォルトで採用されています。


CoffeeScriptのインストールは、同じように

    npm intall -g coffee-script

としてインストールできます。


これで、nodeと同じようにcoffeescriptもTerminal上で試すことができるようになりました。

JavaScriptとCoffeeScriptの違いはたとえば、次のような例で見ることができます。

JavaScriptで、1から10まで配列を作って、それを足し合わせるというのをやると

    var items = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
    var total = 0;

    for ( i = 0 ; i < items.length; i++) {
      total += items[i];
    }

    console.log(total);

CoffeeScriptの場合

    items = [1..10]
    total = 0

    for item in items
      total += item

    console.log total


となります。


参考URL

- [Wikipedia : CoffeeScript](http://ja.wikipedia.org/wiki/CoffeeScript)
- [GitHub : isaacs/npm](https://github.com/isaacs/npm)
- [GitHub : visionmedia/express](https://github.com/visionmedia/express)
- [GitHub : jashkenas/coffee-script](https://github.com/jashkenas/coffee-script)
- [npm : npmの公式サイト](https://npmjs.org)
- [Express - Node.js Web Application Framework : Expressの公式サイト](http://expressjs.com)
- [CoffeeScript ; CoffeeScriptの公式サイト](http://coffeescript.org)
- [js2coffee - Convert JavaScript Code to CoffeeScript : JavaScriptをCoffeeScriptに翻訳できるサイト](http://js2coffee.org)



