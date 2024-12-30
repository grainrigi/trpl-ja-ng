<!--
# Introduction
-->
# イントロダクション

<!--
> Note: This edition of the book is the same as [The Rust Programming
> Language][nsprust] available in print and ebook format from [No Starch
> Press][nsp].
-->
> 注: この本は、書籍として利用可能な[The Rust Programming Language][nsprust]と、
> [No Starch Press][nsp]のebook形式と同じです。

[nsprust]: https://nostarch.com/rust-programming-language-2nd-edition
[nsp]: https://nostarch.com/

<!--
Welcome to _The Rust Programming Language_, an introductory book about Rust.
The Rust programming language helps you write faster, more reliable software.
High-level ergonomics and low-level control are often at odds in programming
language design; Rust challenges that conflict. Through balancing powerful
technical capacity and a great developer experience, Rust gives you the option
to control low-level details (such as memory usage) without all the hassle
traditionally associated with such control.
-->
*The Rust Programming Language*へようこそ。この本はRustの入門書です。
Rustプログラミング言語は、より高速で信頼性の高いソフトウェアを記述する手助けをします。
プログラミング言語設計において、高レベルの記述容易性と低レベルの制御は相反するものとなりがちですが、Rustはその対立に挑戦します。
Rustは、強力な技術的能力と優れた開発者体験のバランスを取ることによって、この手の制御に元来つきものだった様々な煩わしさを回避しつつ、低レベルの詳細（メモリ使用量など）を制御する選択肢を提供します。

<!--
## Who Rust Is For
-->
## Rustは誰のためのものか

<!--
Rust is ideal for many people for a variety of reasons. Let’s look at a few of
the most important groups.
-->
Rustは、さまざまな理由から多くの人々にとって理想的な言語です。特に重要なグループをいくつか見てみましょう。

<!--
### Teams of Developers
-->
### 開発者チーム

<!--
Rust is proving to be a productive tool for collaborating among large teams of
developers with varying levels of systems programming knowledge. Low-level code
is prone to various subtle bugs, which in most other languages can be caught
only through extensive testing and careful code review by experienced
developers. In Rust, the compiler plays a gatekeeper role by refusing to
compile code with these elusive bugs, including concurrency bugs. By working
alongside the compiler, the team can spend their time focusing on the program’s
logic rather than chasing down bugs.
-->
Rustは、大規模な開発チームにおいて、システムプログラミングに関して様々な知識レベルの開発者が混在する場合に、コラボレーションのための生産的なツールとなることが証明されてきました。
低レベルのコードでは微妙なバグが発生しやすく、他の多くの言語では、広範なテストや経験豊富な開発者による慎重なコードレビューを行って初めてこれらのバグを検出することができます。
Rustでは、コンパイラが門番の役割を果たし、これらの捉えにくいバグ、特に並行性に関するバグが含まれるコードをコンパイルすることを拒否します。
コンパイラと連携することで、チームはバグの追跡に時間を費やすのではなく、プログラムのロジックに集中することができます。

<!--
Rust also brings contemporary developer tools to the systems programming world:
-->
また、Rustはシステムプログラミングの世界に現代的な開発ツールをもたらします。

<!--
- Cargo, the included dependency manager and build tool, makes adding,
  compiling, and managing dependencies painless and consistent across the Rust
  ecosystem.
- The Rustfmt formatting tool ensures a consistent coding style across
  developers.
- The rust-analyzer powers Integrated Development Environment (IDE)
  integration for code completion and inline error messages.
-->
- Cargoは、付属の依存関係管理ツール兼ビルドツールで、依存関係の追加、コンパイル、管理を容易にし、Rustのエコシステム全体で一貫性を持たせます。
- Rustfmtフォーマットツールは開発者の間で一貫したコーディングスタイルを保証します。
- rust-analyzerは、IDE(統合開発環境)との統合により、コード補完やインラインエラーメッセージに対応しています。

<!--
By using these and other tools in the Rust ecosystem, developers can be
productive while writing systems-level code.
-->
これらのツールやRustエコシステムの他のツールを使用することで、開発者はシステムレベルのコードを書きながら生産性を高めることができます。

<!--
### Students
-->
### 学生

<!--
Rust is for students and those who are interested in learning about systems
concepts. Using Rust, many people have learned about topics like operating
systems development. The community is very welcoming and happy to answer
student questions. Through efforts such as this book, the Rust teams want to
make systems concepts more accessible to more people, especially those new to
programming.
-->
Rustは、学生やシステムの概念について学びたい人々に向いています。
Rustを使って、多くの人々がオペレーティングシステムの開発などのトピックについて学んできました。
コミュニティは非常に友好的で、学生からの質問にも喜んで答えます。
この本のような取り組みを通じて、Rustのチームはシステムに関する概念をより多くの人々、特にプログラミング初心者がアクセスしやすくしたいと考えています。

<!--
### Companies
-->
### 企業

<!--
Hundreds of companies, large and small, use Rust in production for a variety of
tasks, including command line tools, web services, DevOps tooling, embedded
devices, audio and video analysis and transcoding, cryptocurrencies,
bioinformatics, search engines, Internet of Things applications, machine
learning, and even major parts of the Firefox web browser.
-->

何百もの大小さまざまな企業が、Rustを本番環境でさまざまなタスクに使用しています。
これには、コマンドラインツール、ウェブサービス、DevOpsツール開発、組み込み機器、音声および映像の解析・トランスコーディング、
暗号通貨、バイオインフォマティクス、検索エンジン、IoTアプリケーション、機械学習、さらにはFirefoxウェブブラウザの主要部分も含まれます。

<!--
### Open Source Developers
-->
### オープンソース開発者

<!--
Rust is for people who want to build the Rust programming language, community,
developer tools, and libraries. We’d love to have you contribute to the Rust
language.
-->
Rustは、Rustプログラミング言語やコミュニティ、開発者ツール、ライブラリの構築に関わりたい人々に向いています。
私たちは、あなたがRust言語に貢献されることを心よりお待ちしております。

<!--
### People Who Value Speed and Stability
-->
### 速度と安定性に価値を見出す方

<!--
Rust is for people who crave speed and stability in a language. By speed, we
mean both how quickly Rust code can run and the speed at which Rust lets you
write programs. The Rust compiler’s checks ensure stability through feature
additions and refactoring. This is in contrast to the brittle legacy code in
languages without these checks, which developers are often afraid to modify. By
striving for zero-cost abstractions, higher-level features that compile to
lower-level code as fast as code written manually, Rust endeavors to make safe
code be fast code as well.
-->

Rustは、言語において速度と安定性を求める人々に向いています。
速度とは、Rustのコードがどれだけ速く実行できるか、またあなたがRustでコードをどれだけ速く記述できるかの両方を指します。
Rustのコンパイラのチェックは、機能の追加やリファクタリングにおける安定性を保証します。
これは、このようなチェック機能がない言語のレガシーコードが脆弱で、開発者が修正することを恐れがちだったのとは対照的です。
Rustはゼロコスト抽象化を追求し、高レベルの機能が手書きのコードと同じ速さの低レベルのコードにコンパイルされるよう努めることで、安全なコードが同時に高速なコードでもあることを目指しています。

<!--
The Rust language hopes to support many other users as well; those mentioned
here are merely some of the biggest stakeholders. Overall, Rust’s greatest
ambition is to eliminate the trade-offs that programmers have accepted for
decades by providing safety _and_ productivity, speed _and_ ergonomics. Give
Rust a try and see if its choices work for you.
-->
Rust言語は他にも多くのユーザーをサポートできればと考えています。
ここで挙げたのは、その中でも特に大きなステークホルダーに過ぎません。
全体として、Rustの最大の野望は、安全性*と*生産性、速度*と*使いやすさを両立させることで、プログラマーが何十年も受け入れてきたトレードオフを排除することです。
Rustを試して、Rustの行った選択があなたに合うか確かめてみてください。

<!--
## Who This Book Is For
-->
## この本の対象読者

<!--
This book assumes that you’ve written code in another programming language but
doesn’t make any assumptions about which one. We’ve tried to make the material
broadly accessible to those from a wide variety of programming backgrounds. We
don’t spend a lot of time talking about what programming _is_ or how to think
about it. If you’re entirely new to programming, you would be better served by
reading a book that specifically provides an introduction to programming.
-->
この本は、他のプログラミング言語でコードを書いたことがあることを前提としていますが、どの言語であるかについては特に前提を置いていません。
私たちは、さまざまなプログラミングの背景を持つ方々が広く利用できるよう、内容を工夫しています。
プログラミングが何であるかや、どのように考えるべきかについては多くを語りません。
もしあなたが全くのプログラミング初心者であれば、プログラミングの入門に特化した本を読むほうが役に立つでしょう。

<!--
## How to Use This Book
-->

<!--
In general, this book assumes that you’re reading it in sequence from front to
back. Later chapters build on concepts in earlier chapters, and earlier
chapters might not delve into details on a particular topic but will revisit
the topic in a later chapter.
-->
基本的に、この本は最初から順番に読むことを前提としています。
後の章は前の章で紹介された概念を基に進んでいきます。
また、前の方の章で特定のトピックに軽くしか触れないことがありますが、その場合、後の章でそのトピックを再度詳しく取り上げます。

<!--
You’ll find two kinds of chapters in this book: concept chapters and project
chapters. In concept chapters, you’ll learn about an aspect of Rust. In project
chapters, we’ll build small programs together, applying what you’ve learned so
far. Chapters 2, 12, and 21 are project chapters; the rest are concept chapters.
-->
この本には2種類の章があります: 概念章とプロジェクト章です。
概念章では、Rustの一つの側面について学びます。
プロジェクト章では、それまでに学んだことを活かして、小さなプログラムを一緒に作成します。
第2章、第12章、第21章がプロジェクト章で、その他の章は概念章です。

<!--
Chapter 1 explains how to install Rust, how to write a “Hello, world!” program,
and how to use Cargo, Rust’s package manager and build tool. Chapter 2 is a
hands-on introduction to writing a program in Rust, having you build up a
number guessing game. Here we cover concepts at a high level, and later
chapters will provide additional detail. If you want to get your hands dirty
right away, Chapter 2 is the place for that. Chapter 3 covers Rust features
that are similar to those of other programming languages, and in Chapter 4
you’ll learn about Rust’s ownership system. If you’re a particularly meticulous
learner who prefers to learn every detail before moving on to the next, you
might want to skip Chapter 2 and go straight to Chapter 3, returning to Chapter
2 when you’d like to work on a project applying the details you’ve learned.
-->
第1章では、Rustのインストール方法、"Hello, world!"プログラムの書き方、Rustのパッケージマネージャー兼ビルドツールであるCargoの使い方を説明します。
第2章は、Rustでプログラムを書くためのハンズオンで、数当てゲームを作成します。
ここでは概念をざっくりと扱い、後の章でさらに詳しく説明します。
すぐに手を動かしたいのであれば、第2章は良い開始点となるでしょう。
第3章では、Rustの他のプログラミング言語と似た特徴を扱い、第4章ではRustの所有権システムについて学びます。
もしあなたが几帳面な学習者で、すべての詳細を学んでから次に進みたいと考えているのであれば、第2章を飛ばしてそのまま第3章に進み、
学んだ詳細を実際のプロジェクトに適用したくなったら第2章に戻るのが良いかもしれません。

<!--
Chapter 5 discusses structs and methods, and Chapter 6 covers enums, `match`
expressions, and the `if let` control flow construct. You’ll use structs and
enums to make custom types in Rust.
-->
第5章では、構造体(struct)とメソッドについて説明し、第6章では列挙型(enum)、`match`式、そして`if let`制御フロー構造について扱います。
Rustでカスタム方を作成するのに、構造体と列挙型を使うことになるでしょう。

<!--
In Chapter 7, you’ll learn about Rust’s module system and about privacy rules
for organizing your code and its public Application Programming Interface
(API). Chapter 8 discusses some common collection data structures that the
standard library provides, such as vectors, strings, and hash maps. Chapter 9
explores Rust’s error-handling philosophy and techniques.
-->
第7章では、コードの整理や公開APIを扱うために、Rustのモジュールシステムとプライバシールールについて学びます。
第8章では、ベクター、文字列、ハッシュマップなどの、標準ライブラリが提供する一般的なコレクションデータ構造について説明します。
第9章では、Rustのエラーハンドリングの哲学と技術を探究します。

<!--
Chapter 10 digs into generics, traits, and lifetimes, which give you the power
to define code that applies to multiple types. Chapter 11 is all about testing,
which even with Rust’s safety guarantees is necessary to ensure your program’s
logic is correct. In Chapter 12, we’ll build our own implementation of a subset
of functionality from the `grep` command line tool that searches for text
within files. For this, we’ll use many of the concepts we discussed in the
previous chapters.
-->
第10章では、ジェネリクス、トレイト、ライフタイムについて詳しく学び、複数の型に適用できるコードを定義する力を得ます。
第11章はテストに関するすべてです。Rustの安全性保証があっても、プログラムのロジックが正しいことを確認するためにはテストが必要です。
第12章では、grepコマンドラインツールの一部機能を実装し、ファイル内のテキストを検索するプログラムを作成します。
この章では、それまでの章で学んだ多くの概念を活用します。

<!--
Chapter 13 explores closures and iterators: features of Rust that come from
functional programming languages. In Chapter 14, we’ll examine Cargo in more
depth and talk about best practices for sharing your libraries with others.
Chapter 15 discusses smart pointers that the standard library provides and the
traits that enable their functionality.
-->
第13章では、関数型プログラミング由来のRustの機能であるクロージャとイテレータについて探究します。
第14章では、Cargoについてさらに深く掘り下げ、ライブラリを他の人と共有するためのベストプラクティスについて語ります。
第15章では、標準ライブラリが提供するスマートポインタと、それらの機能を実現するトレイトについて説明します。

<!--
In Chapter 16, we’ll walk through different models of concurrent programming and
talk about how Rust helps you to program in multiple threads fearlessly. In
Chapter 17, we will build on that by exploring Rust’s async and await syntax and
the lightweight concurrency model they support.
-->
第16章では、さまざまな並行プログラミングのモデルを紹介し、Rustがどのようにしてマルチスレッドのプログラムを恐れなく書く手助けをするかについて解説します。
第17章ではさらに進んで、Rustのasync/await構文とそれがサポートする軽量な並行モデルについて探究します。

<!--
Chapter 18 looks at how Rust idioms compare to object-oriented programming
principles you might be familiar with.
-->
第18章では、Rustのイディオムが、あなたが馴染みのあるオブジェクト指向プログラミングの原則と比較してどうであるかについて見ていきます。

<!--
Chapter 19 is a reference on patterns and pattern matching, which are powerful
ways of expressing ideas throughout Rust programs. Chapter 20 contains a
smorgasbord of advanced topics of interest, including unsafe Rust, macros, and
more about lifetimes, traits, types, functions, and closures.
-->
第19章は、パターンとパターンマッチングのリファレンスです。これらはRustプログラム全体を通してアイデアを表現する強力な方法です。
第20章では、unsafe Rustやマクロ、そして、ライフタイム、トレイト、型、関数、クロージャに関するさらに詳しい内容など、さまざまな高度なトピックを取り上げます。

<!--
In Chapter 21, we’ll complete a project in which we’ll implement a low-level
multithreaded web server!
-->
第21章では、低レベルのマルチスレッドのウェブサーバーを実装するプロジェクトを完了します！

<!--
Finally, some appendices contain useful information about the language in a
more reference-like format. Appendix A covers Rust’s keywords, Appendix B
covers Rust’s operators and symbols, Appendix C covers derivable traits
provided by the standard library, Appendix D covers some useful development
tools, and Appendix E explains Rust editions. In Appendix F, you can find
translations of the book, and in Appendix G we’ll cover how Rust is made and
what nightly Rust is.
-->
最後に、いくつかの付録には、言語に関する有用な情報がよりリファレンスライクな形式で含まれています。
付録AではRustのキーワード、付録BではRustの演算子と記号、付録Cでは標準ライブラリが提供する導出可能なトレイト、付録Dでは便利な開発ツール、付録EではRustのエディションについて網羅されています。
付録Fには本書の翻訳が掲載され、付録GではRustがどう作られているかについてと、nightly Rustがなんであるかについて解説します。

<!--
There is no wrong way to read this book: if you want to skip ahead, go for it!
You might have to jump back to earlier chapters if you experience any
confusion. But do whatever works for you.
-->
この本の読み方に間違いはありません。飛ばして先に進みたい場合は、ぜひそうしてください！
もし途中で混乱することがあれば、前の章に戻ることがあるかもしれませんが、自分に合った方法で進めてください。

<span id="ferris"></span>

<!--
An important part of the process of learning Rust is learning how to read the
error messages the compiler displays: these will guide you toward working code.
As such, we’ll provide many examples that don’t compile along with the error
message the compiler will show you in each situation. Know that if you enter
and run a random example, it may not compile! Make sure you read the
surrounding text to see whether the example you’re trying to run is meant to
error. Ferris will also help you distinguish code that isn’t meant to work:
-->
Rustを学ぶ過程で重要な部分の一つは、コンパイラが表示するエラーメッセージの読み方を学ぶことです。
これらのメッセージは、あなたを動作するコードへと導いてくれます。
そのため、たくさんのコンパイルできない例をその際にコンパイラが表示するエラーメッセージと一緒に紹介します。
適当な例を入力して実行しても、コンパイルできないかもしれない点に注意してください！
実行しようとしている例がエラーを意図しているかどうかを確認するために、周囲のテキストをよく読んでください。
Ferrisも、動作しないことが意図されているコードを見分ける手助けをしてくれます。

<!--
| Ferris                                                                                                           | Meaning                                          |
| ---------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ |
| <img src="img/ferris/does_not_compile.svg" class="ferris-explain" alt="Ferris with a question mark"/>            | This code does not compile!                      |
| <img src="img/ferris/panics.svg" class="ferris-explain" alt="Ferris throwing up their hands"/>                   | This code panics!                                |
| <img src="img/ferris/not_desired_behavior.svg" class="ferris-explain" alt="Ferris with one claw up, shrugging"/> | This code does not produce the desired behavior. |
-->
| Ferris                                                                                                                 | Meaning                                    |
| ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------ |
| <img src="img/ferris/does_not_compile.svg" class="ferris-explain" alt="疑問符付きのFerris"/>                           | このコードはコンパイルできません！         |
| <img src="img/ferris/panics.svg" class="ferris-explain" alt="両手を上げているFerris"/>                                 | このコードはパニックします！               |
| <img src="img/ferris/not_desired_behavior.svg" class="ferris-explain" alt="片方のツメを上げて肩をすくめているFerris"/> | このコードは意図したとおりに動作しません。 |

<!--
In most situations, we’ll lead you to the correct version of any code that
doesn’t compile.
-->
ほとんどの状況では、コンパイルできないコードが正しく動作するよう我々が誘導します。

<!--
## Source Code
-->
## ソースコード

<!--
The source files from which this book is generated can be found on
[GitHub][book].
-->
この本の生成に使用されているソースファイルは、[GitHub][book]にあります。

> 訳注: 日本語版は[こちら][book-ja]です。

[book]: https://github.com/rust-lang/book/tree/main/src
[book-ja]: https://github.com/rust-lang-ja/book-ja