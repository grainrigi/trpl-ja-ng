<!--
## Installation
-->
## インストール

<!--
The first step is to install Rust. We’ll download Rust through `rustup`, a
command line tool for managing Rust versions and associated tools. You’ll need
an internet connection for the download.
-->
最初のステップはRustをインストールすることです。
今回は、`rustup`というRustのバージョンや関連ツールを管理するためのコマンドラインツールを通してRustをダウンロードします。
ダウンロードにはインターネット接続が必要です。

<!--
> Note: If you prefer not to use `rustup` for some reason, please see the
> [Other Rust Installation Methods page][otherinstall] for more options.
-->
> 注: 何らかの理由で`rustup`を使用したくない場合は、[他のRustインストール方法のページ][otherinstall]を参照してください。

<!--
The following steps install the latest stable version of the Rust compiler.
Rust’s stability guarantees ensure that all the examples in the book that
compile will continue to compile with newer Rust versions. The output might
differ slightly between versions because Rust often improves error messages and
warnings. In other words, any newer, stable version of Rust you install using
these steps should work as expected with the content of this book.
-->
以下に示す手順により、Rustコンパイラの最新の安定版がインストールされます。
Rustの安定性保証により、本書でコンパイル可能なすべての例は、新しいRustバージョンでも引き続きコンパイルできることが保証されます。
Rustはエラーメッセージや警告を頻繁に改善しているため、出力はバージョン間で若干異なる場合があります。
言い換えれば、ここで紹介した手順によってより新しいバージョンの安定版Rustがインストールされても、本書の内容で期待される通りに動作するはずです。

<!--
> ### Command Line Notation
>
> In this chapter and throughout the book, we’ll show some commands used in the
> terminal. Lines that you should enter in a terminal all start with `$`. You
> don’t need to type the `$` character; it’s the command line prompt shown to
> indicate the start of each command. Lines that don’t start with `$` typically
> show the output of the previous command. Additionally, PowerShell-specific
> examples will use `>` rather than `$`.
-->
> ### コマンドラインの表記
>
> この章および本書全体で、ターミナルで使用するいくつかのコマンドを示します。
> ターミナルで入力する必要がある行はすべて`$`で始まります。
> `$`記号を入力する必要はありません；これは各コマンドの開始を示すコマンドラインのプロンプトです。
> `$`で始まらない行は、通常、前のコマンドの出力を示します。
> また、PowerShell固有の例では、`$`の代わりに`>`を使用します。

<!--
### Installing `rustup` on Linux or macOS
-->
### LinuxまたはmacOSに`rustup`をインストールする

<!--
If you’re using Linux or macOS, open a terminal and enter the following command:
-->
あなたがLinuxまたはmacOSを使用している場合、ターミナルを開いて以下のコマンドを入力してください。

```console
$ curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
```

<!--
The command downloads a script and starts the installation of the `rustup`
tool, which installs the latest stable version of Rust. You might be prompted
for your password. If the install is successful, the following line will appear:
-->
このコマンドはスクリプトをダウンロードし、`rustup`ツールのインストールを開始します。
`rustup`はRustの最新の安定版をインストールします。
インストール中にパスワードの入力を求められるかもしれません。
インストールが成功すると、以下のようなメッセージが表示されます。

```text
Rust is installed now. Great!
```

<!--
You will also need a _linker_, which is a program that Rust uses to join its
compiled outputs into one file. It is likely you already have one. If you get
linker errors, you should install a C compiler, which will typically include a
linker. A C compiler is also useful because some common Rust packages depend on
C code and will need a C compiler.
-->
また、これに加えて*リンカー*が必要となります。これは、Rustがコンパイルした出力を1つのファイルに結合するために使用するプログラムです。
多くの場合、すでにリンカーはインストールされているはずです。
リンカーエラーが発生した場合は、Cコンパイラをインストールする必要があります。Cコンパイラには通常リンカーも含まれているためです。
また、いくつかの一般的なRustパッケージがCコードに依存しており、Cコンパイラが必要になることがあるため、入れておくと便利でしょう。

<!--
On macOS, you can get a C compiler by running:
-->
macOSでは、次のコマンドを実行することでCコンパイラをインストールできます。

```console
$ xcode-select --install
```

<!--
Linux users should generally install GCC or Clang, according to their
distribution’s documentation. For example, if you use Ubuntu, you can install
the `build-essential` package.
-->
Linuxユーザーは、一般的にはGCCまたはClangをインストールすればよいでしょう。
自分のディストリビューションのドキュメントに従ってインストールを行ってください。
例えば、Ubuntuを使用している場合、`build-essential`パッケージをインストールすることができます。

<!--
### Installing `rustup` on Windows
-->
### Windowsに`rustup`をインストールする

<!--
On Windows, go to [https://www.rust-lang.org/tools/install][install] and follow
the instructions for installing Rust. At some point in the installation, you’ll
be prompted to install Visual Studio. This provides a linker and the native
libraries needed to compile programs. If you need more help with this step, see
[https://rust-lang.github.io/rustup/installation/windows-msvc.html][msvc]
-->
Windowsでは、[https://www.rust-lang.org/tools/install][install] にアクセスして、Rustのインストール手順に従ってください。
インストールの途中で、Visual Studioのインストールを求められるでしょう。
これにより、プログラムをコンパイルするために必要なリンカーとネイティブライブラリが提供されます。
このステップでさらに助けが必要な場合は、[https://rust-lang.github.io/rustup/installation/windows-msvc.html][msvc] を参照してください。

<!--
The rest of this book uses commands that work in both _cmd.exe_ and PowerShell.
If there are specific differences, we’ll explain which to use.
-->
本書の残りの部分では、*cmd.exe* と PowerShell の両方で動作するコマンドを使用します。
特定の違いがある場合は、どちらを使用すべきかを説明します。

<!--
### Troubleshooting
-->
### トラブルシューティング

<!--
To check whether you have Rust installed correctly, open a shell and enter this
line:
-->

Rustが正しくインストールされているかを確認するには、シェルを開いて以下のコマンドを入力してください。

```console
$ rustc --version
```

<!--
You should see the version number, commit hash, and commit date for the latest
stable version that has been released, in the following format:
-->
以下の形式で、最新の安定版Rustのバージョン番号、コミットハッシュ、およびコミット日が表示されるはずです。

```text
rustc x.y.z (abcabcabc yyyy-mm-dd)
```

<!--
If you see this information, you have installed Rust successfully! If you don’t
see this information, check that Rust is in your `%PATH%` system variable as
follows.
-->
この情報が表示されれば、Rustは正常にインストールされています！
もし表示されない場合は、Rustがシステムの`%PATH%`環境変数に含まれているかどうかを確認してください。
確認方法は以下の通りです。

Windows CMDの場合、

```console
> echo %PATH%
```

Powershellの場合、

```powershell
> echo $env:Path
```

LinuxまたはmacOSの場合、

```console
$ echo $PATH
```

<!--
If that’s all correct and Rust still isn’t working, there are a number of
places you can get help. Find out how to get in touch with other Rustaceans (a
silly nickname we call ourselves) on [the community page][community].
-->
もし上記の設定が正しいにも関わらずまだRustが動作しない場合は、いくつかの方法でサポートを受けることができます。
他のRustacean（Rustユーザが自分たちのことを呼ぶ、冗談めいたニックネーム）たちと連絡を取る方法については、[コミュニティページ][community]を確認してください。

> 訳注：Rustaceanについて、いらないかもしれない補足です。[公式Twitter曰く、Rustaceanはcrustaceans（甲殻類）から来ている][twitter]そうです。
> そのため、Rustのマスコットは（非公式らしいですが）[カニ][mascott]。上の会話でCの欠点を削ぎ落としているからcを省いてるの？みたいなことを聞いていますが、
> 違うそうです。検索したら、堅牢性が高いから甲殻類という意見もありますが、真偽は不明です。
> 明日使えるかもしれないトリビアでした。

<!--
### Updating and Uninstalling
-->
### アップデートおよびアンインストール

<!--
Once Rust is installed via `rustup`, updating to a newly released version is
easy. From your shell, run the following update script:
-->
一度Rustを`rustup`でインストールしてしまえば、新しいバージョンへの更新は簡単にできます。
シェルから以下のアップデートスクリプトを実行してください。

```console
$ rustup update
```

<!--
To uninstall Rust and `rustup`, run the following uninstall script from your
shell:
-->
Rustと`rustup`をアンインストールするには、シェルから以下のアンインストールスクリプトを実行してください。

```console
$ rustup self uninstall
```

<!--
### Local Documentation
-->
### ローカルドキュメント

<!--
The installation of Rust also includes a local copy of the documentation so
that you can read it offline. Run `rustup doc` to open the local documentation
in your browser.
-->
Rustのインストールには、オフラインで読めるようにドキュメントのローカルコピーが含まれています。
ブラウザでローカルのドキュメントを開くには、`rustup doc` を実行してください。

<!--
Any time a type or function is provided by the standard library and you’re not
sure what it does or how to use it, use the application programming interface
(API) documentation to find out!
-->
標準ライブラリによって提供される型や関数について、それが何であるかやどう使うかがわからない場合は、
アプリケーションプログラミングインターフェース（API）ドキュメントを参照して確認しましょう！

<!--
### Text Editors and Integrated Development Environments
-->
### テキストエディタと統合開発環境

<!--
This book makes no assumptions about what tools you use to author Rust code.
Just about any text editor will get the job done! However, many text editors and
integrated development environments (IDEs) have built-in support for Rust. You
can always find a fairly current list of many editors and IDEs on [the tools
page][tools] on the Rust website.
-->
この本では、Rustコードを作成するために使用するツールについては特に前提を設けていません。
ほとんどのテキストエディタで作業は可能です！
ただし、多くのテキストエディタや統合開発環境（IDE）はRustをサポートしています。
Rustの公式ウェブサイトの[ツールページ][tools]で、多くのエディタやIDEの最新のリストを確認できます。

[otherinstall]: https://forge.rust-lang.org/infra/other-installation-methods.html
[install]: https://www.rust-lang.org/tools/install
[msvc]: https://rust-lang.github.io/rustup/installation/windows-msvc.html
[community]: https://www.rust-lang.org/community
[tools]: https://www.rust-lang.org/tools
[twitter]: https://mobile.twitter.com/rustlang/status/916284650674323457
[mascott]: https://www.slideshare.net/wolf-dog/ss-64026540
