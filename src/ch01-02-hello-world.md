## Hello, World!

<!--
Now that you’ve installed Rust, it’s time to write your first Rust program.
It’s traditional when learning a new language to write a little program that
prints the text `Hello, world!` to the screen, so we’ll do the same here!
-->
Rustをインストールしたので、さっそく最初のRustプログラムを書いてみましょう。
新しい言語を学ぶ際には、画面に「Hello, world!」と表示する小さなプログラムを書くのが伝統です。
なので、ここでも同じことをしてみましょう！

<!--
> Note: This book assumes basic familiarity with the command line. Rust makes
> no specific demands about your editing or tooling or where your code lives, so
> if you prefer to use an integrated development environment (IDE) instead of
> the command line, feel free to use your favorite IDE. Many IDEs now have some
> degree of Rust support; check the IDE’s documentation for details. The Rust
> team has been focusing on enabling great IDE support via `rust-analyzer`. See
> [Appendix D][devtools] for more details.
-->
> 注意: この本では、コマンドラインの基本的な知識があることを前提としています。
> Rustは、コードエディタやツール、またはコードの配置場所について特に制約を設けていないため、
> コマンドラインではなく統合開発環境（IDE）を使用したい場合は、お気に入りのIDEを自由に使ってください。
> 現在、多くのIDEがRustをある程度サポートしています。
> 詳細については、使用しているIDEのドキュメントを確認してください。
> Rustチームは、`rust-analyzer`を通じて優れたIDEサポートを実現することに注力しています。
> 詳細については[付録D][devtools]をご覧ください。

<!--
### Creating a Project Directory
-->
### プロジェクトディレクトリを作成する

<!--
You’ll start by making a directory to store your Rust code. It doesn’t matter
to Rust where your code lives, but for the exercises and projects in this book,
we suggest making a _projects_ directory in your home directory and keeping all
your projects there.
-->
まず、Rustのコードを保存するためのディレクトリを作成しましょう。
コードの保存場所がどこであってもRustにとっては関係がないのですが、この本の練習問題やプロジェクトを進めるにあたっては、
ホームディレクトリ内に _projects_ ディレクトリを作成し、すべてのプロジェクトをそこに保存することをお勧めします。

<!--
Open a terminal and enter the following commands to make a _projects_ directory
and a directory for the “Hello, world!” project within the _projects_ directory.
-->
ターミナルを開き、以下のコマンドを入力して _projects_ ディレクトリを作成し、その中に「Hello, world!」プロジェクト用のディレクトリを作成してください。


<!--
For Linux, macOS, and PowerShell on Windows, enter this:
-->
Linux, macOS, WindowsのPowershellの場合、以下を入力してください。

```console
$ mkdir ~/projects
$ cd ~/projects
$ mkdir hello_world
$ cd hello_world
```

<!--
For Windows CMD, enter this:
-->
Windows CMDの場合、以下を入力してください。

```cmd
> mkdir "%USERPROFILE%\projects"
> cd /d "%USERPROFILE%\projects"
> mkdir hello_world
> cd hello_world
```

<!--
### Writing and Running a Rust Program
-->
### Rustプログラムを記述・実行する

<!--
Next, make a new source file and call it _main.rs_. Rust files always end with
the _.rs_ extension. If you’re using more than one word in your filename, the
convention is to use an underscore to separate them. For example, use
_hello_world.rs_ rather than _helloworld.rs_.
-->
次に、新しいソースファイルを作成し、_main.rs_ という名前を付けてください。
Rust のファイル名は必ず _.rs_ 拡張子で終わります。
ファイル名が複数の単語で構成される場合は、単語をアンダースコアで区切るのが慣例です。
たとえば、_helloworld.rs_ ではなく _hello_world.rs_ を使用します。

<!--
Now open the _main.rs_ file you just created and enter the code in Listing 1-1.
-->
それでは、先ほど作成した _main.rs_ ファイルを開き、リスト 1-1 のコードを入力してください。

<Listing number="1-1" file-name="main.rs" caption="`Hello, world!`を出力するプログラム">

```rust
fn main() {
    println!("Hello, world!");
}
```

</Listing>

<!--
Save the file and go back to your terminal window in the
_~/projects/hello_world_ directory. On Linux or macOS, enter the following
commands to compile and run the file:
-->
ファイルを保存したら、_~/projects/hello_world_ のターミナルウィンドウに戻ります。
Linux または macOS の場合、次のコマンドを入力してファイルをコンパイルし、実行してください。

```console
$ rustc main.rs
$ ./main
Hello, world!
```

<!--
On Windows, enter the command `.\main.exe` instead of `./main`:
-->
Windowsの場合、`./main`の代わりに`.\main.exe`コマンドを入力してください。

```powershell
> rustc main.rs
> .\main.exe
Hello, world!
```

<!--
Regardless of your operating system, the string `Hello, world!` should print to
the terminal. If you don’t see this output, refer back to the
[“Troubleshooting”][troubleshooting] part of the Installation
section for ways to get help.
-->
使用しているオペレーティングシステムに関係なく、ターミナルに文字列 `Hello, world!` が出力されるはずです。
この出力が表示されない場合は、インストール節の[「トラブルシューティング」][troubleshooting]を参照して解決方法を確認してください。

<!--
If `Hello, world!` did print, congratulations! You’ve officially written a Rust
program. That makes you a Rust programmer—welcome!
-->
`Hello, world!` が表示されたなら、おめでとうございます！
あなたは正式にRustプログラムを書いたことになります。
これであなたもRustプログラマーです—ようこそ！

<!--
### Anatomy of a Rust Program
-->
### Rustプログラムの構造

<!--
Let’s review this “Hello, world!” program in detail. Here’s the first piece of
the puzzle:
-->
「Hello, world!」プログラムを詳しく見ていきましょう。まずはパズルの最初の部分です。

```rust
fn main() {

}
```

<!--
These lines define a function named `main`. The `main` function is special: it
is always the first code that runs in every executable Rust program. Here, the
first line declares a function named `main` that has no parameters and returns
nothing. If there were parameters, they would go inside the parentheses `()`.
-->
これらの行は`main`という名前の関数を定義しています。
`main`関数は特別で、Rustプログラムの実行可能ファイルでは常に`main`関数が最初に実行されるコードになります。
ここでは、引数を取らず、戻り値もない`main`という関数が最初の行で宣言されています。
もし引数があれば、それらは括弧`()`内に記述されます。

<!--
The function body is wrapped in `{}`. Rust requires curly brackets around all
function bodies. It’s good style to place the opening curly bracket on the same
line as the function declaration, adding one space in between.
-->
関数の本体は`{}`で囲まれています。
Rustでは、すべての関数の本体は波括弧で囲う必要があります。
開き波括弧は関数宣言と同じ行に配置し、その間に1つスペースを入れるのが良いスタイルです。

<!--
> Note: If you want to stick to a standard style across Rust projects, you can
> use an automatic formatter tool called `rustfmt` to format your code in a
> particular style (more on `rustfmt` in
> [Appendix D][devtools]). The Rust team has included this tool
> with the standard Rust distribution, as `rustc` is, so it should already be
> installed on your computer!
-->
> 注: Rustプロジェクト間で一貫したスタイルを適用したい場合、`rustfmt`という自動フォーマッターツールを使用して、特定のスタイルでコードを整形できます
> （`rustfmt`について詳しくは[Appendix D][devtools]を参照）。
> Rustチームはこのツールを標準のRustディストリビューションに含めており、`rustc`と同様に、すでにコンピュータにインストールされているはずです！

<!--
The body of the `main` function holds the following code:
-->
`main` 関数の本体には以下のコードが含まれています。

```rust
println!("Hello, world!");
```

<!--
This line does all the work in this little program: it prints text to the
screen. There are four important details to notice here.
-->
この行がこの小さなプログラムのすべての作業を行います：画面にテキストを表示します。
ここで注目すべき4つの重要な点があります。

<!--
First, `println!` calls a Rust macro. If it had called a function instead, it
would be entered as `println` (without the `!`). We’ll discuss Rust macros in
more detail in Chapter 20. For now, you just need to know that using a `!`
means that you’re calling a macro instead of a normal function and that macros
don’t always follow the same rules as functions.
-->
まず、`println!` はRustのマクロを呼び出しています。
もし関数を呼び出していた場合、`println`（`!`なし）と記述されます。
Rustのマクロについては第20章で詳しく説明しますが、今は `!` を使うことで通常の関数ではなくマクロを呼び出していること、
そしてマクロは関数とは必ずしも同じルールに従わないことを理解しておけば十分です。

<!--
Second, you see the `"Hello, world!"` string. We pass this string as an argument
to `println!`, and the string is printed to the screen.
-->
次に、`"Hello, world!"` という文字列が見えます。
この文字列は `println!` に引数として渡され、画面に表示されます。

<!--
Third, we end the line with a semicolon (`;`), which indicates that this
expression is over and the next one is ready to begin. Most lines of Rust code
end with a semicolon.
-->
第三に、行の最後にセミコロン（`;`）があります。
これは、この式が終了し、次の式が始まる準備ができたことを示します。
Rustコードのほとんどの行はセミコロンで終わります。

<!--
### Compiling and Running Are Separate Steps
-->
### コンパイルと実行は別々のステップである

<!--
You’ve just run a newly created program, so let’s examine each step in the
process.
-->
新しく作成したプログラムを実行したので、一連の過程の各ステップを確認しましょう。

<!--
Before running a Rust program, you must compile it using the Rust compiler by
entering the `rustc` command and passing it the name of your source file, like
this:
-->
Rustプログラムを実行する場合、まずはRustコンパイラを使用してコンパイルする必要があります。
コンパイルするには、以下のように`rustc`コマンドを入力し、ソースファイルの名前を渡します。

```console
$ rustc main.rs
```

<!--
If you have a C or C++ background, you’ll notice that this is similar to `gcc`
or `clang`. After compiling successfully, Rust outputs a binary executable.
-->
CやC++の経験がある方は、これが`gcc`や`clang`に似ていることに気付くでしょう。
コンパイルが成功すると、Rustはバイナリ実行可能ファイルを出力します。

<!--
On Linux, macOS, and PowerShell on Windows, you can see the executable by
entering the `ls` command in your shell:
-->
Linux、macOS、WindowsのPowerShellでは、シェルで`ls`コマンドを入力することで実行可能ファイルを見ることができます。

```console
$ ls
main  main.rs
```

<!--
On Linux and macOS, you’ll see two files. With PowerShell on Windows, you’ll
see the same three files that you would see using CMD. With CMD on Windows, you
would enter the following:
-->
Linux と macOS では、2つのファイルが表示されます。
Windows の PowerShell では、CMD の場合に見るのと同じ3つのファイルが表示されます。
Windows の CMD であれば、次のように入力します。

```cmd
> dir /B %= the /B option says to only show the file names =%
main.exe
main.pdb
main.rs
```

<!--
This shows the source code file with the _.rs_ extension, the executable file
(_main.exe_ on Windows, but _main_ on all other platforms), and, when using
Windows, a file containing debugging information with the _.pdb_ extension.
From here, you run the _main_ or _main.exe_ file, like this:
-->
これにより、_.rs_ 拡張子のソースコードファイル、実行可能ファイル（Windows では _main.exe_、他のプラットフォームでは _main_）、
そして Windows を使用している場合は、_.pdb_ 拡張子のデバッグ情報を含むファイルが表示されます。
ここから、_main_ または _main.exe_ ファイルを次のように実行します。

<!--
```console
$ ./main # or .\main.exe on Windows
```
-->
```console
$ ./main # または、Windowsの場合 .\main.exe
```

<!--
If your _main.rs_ is your “Hello, world!” program, this line prints `Hello,
world!` to your terminal.
-->
もし _main.rs_ が「Hello, world!」プログラムであれば、ターミナルに `Hello, world!` と表示されます。

<!--
If you’re more familiar with a dynamic language, such as Ruby, Python, or
JavaScript, you might not be used to compiling and running a program as
separate steps. Rust is an _ahead-of-time compiled_ language, meaning you can
compile a program and give the executable to someone else, and they can run it
even without having Rust installed. If you give someone a _.rb_, _.py_, or
_.js_ file, they need to have a Ruby, Python, or JavaScript implementation
installed (respectively). But in those languages, you only need one command to
compile and run your program. Everything is a trade-off in language design.
-->
Ruby、Python、JavaScriptのような動的言語に慣れている場合、プログラムのコンパイルと実行が別々の手順であることに馴染みがないかもしれません。
Rustは *事前コンパイル型(ahead-of-time compiled)* の言語であるので、プログラムをコンパイルして実行可能ファイルを他の人に渡すことができ、その人がRustをインストールしていなくてもそのファイルを実行できます。
他の人に _.rb_ 、 _.py_ 、 _.js_ ファイルを渡した場合、それぞれRuby、Python、JavaScriptの実装が相手側にインストールされている必要があります。
しかし、これらの言語では、プログラムをコンパイルして実行するのに1つのコマンドだけで済みます。
すべては言語設計におけるトレードオフです。

<!--
Just compiling with `rustc` is fine for simple programs, but as your project
grows, you’ll want to manage all the options and make it easy to share your
code. Next, we’ll introduce you to the Cargo tool, which will help you write
real-world Rust programs.
-->
単純なプログラムであれば単に`rustc`でコンパイルするのでも問題ないのですが、プロジェクトが大きくなるにつれて、さまざまなオプションを管理し、コードを簡単に共有できるようにしたくなるでしょう。
次は、現実のRustプログラムを作成する際に役立つツール「Cargo」を紹介します。

[troubleshooting]: ch01-01-installation.html#troubleshooting
[devtools]: appendix-04-useful-development-tools.html
