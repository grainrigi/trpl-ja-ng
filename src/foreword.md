<!--
# Foreword
-->
# まえがき

<!--
It wasn’t always so clear, but the Rust programming language is fundamentally
about _empowerment_: no matter what kind of code you are writing now, Rust
empowers you to reach farther, to program with confidence in a wider variety of
domains than you did before.
-->
かつてはそれほど明確ではありませんでしたが、Rustプログラミング言語は『能力拡張(empowerment)』を根本原理としています。
現在どのようなコードを書いているとしても、Rustはあなたの能力を拡張し、これまで以上に自信を持ってより幅広い分野でプログラムを作成できるようにします。

<!--
Take, for example, “systems-level” work that deals with low-level details of
memory management, data representation, and concurrency. Traditionally, this
realm of programming is seen as arcane, accessible only to a select few who
have devoted the necessary years learning to avoid its infamous pitfalls. And
even those who practice it do so with caution, lest their code be open to
exploits, crashes, or corruption.
-->
例えば、メモリ管理、データ表現、並行性といった低レベルの詳細に関わる『システムレベル』の作業を考えてみましょう。
伝統的に、この領域のプログラミングは難解なものとされており、長年の学習を通じてその悪名高い落とし穴を回避する術を身につけた、限られた人々だけが手を伸ばせるものと見なされてきました。
そして、そのような鍛錬を積んだ者でさえ実際の作業は注意深く行い、コードが脆弱性、クラッシュ、あるいはデータ破損の危険にさらされないようにします。

<!--
Rust breaks down these barriers by eliminating the old pitfalls and providing a
friendly, polished set of tools to help you along the way. Programmers who need
to “dip down” into lower-level control can do so with Rust, without taking on
the customary risk of crashes or security holes, and without having to learn
the fine points of a fickle toolchain. Better yet, the language is designed to
guide you naturally towards reliable code that is efficient in terms of speed
and memory usage.
-->
Rustは従来の手法に存在した落とし穴を排除するとともに、使いやすく洗練されたツール群を提供することでこの障壁を取り除いてくれます。
プログラマーがより低いレベルに「下がって」制御を行う必要がある場合でも、
Rustを使うことで、従来のようなクラッシュやセキュリティホールのリスクを抱えることなく、
また扱いづらいツールチェーンの細部を学ぶ必要もなしに目的を達成することができます。
さらに素晴らしいのは、Rustが高速かつメモリ効率の良い信頼性の高いコードへ自然と導いてくれるよう設計されている点です。

<!--
Programmers who are already working with low-level code can use Rust to raise
their ambitions. For example, introducing parallelism in Rust is a relatively
low-risk operation: the compiler will catch the classical mistakes for you. And
you can tackle more aggressive optimizations in your code with the confidence
that you won’t accidentally introduce crashes or vulnerabilities.
-->
すでに低レベルのコードを扱っているプログラマーは、Rustを活用してさらなる高みを目指すことができます。
例えば、Rustで並列処理を導入することは比較的低リスクな操作です。
Rustのコンパイラが古典的なミスを自動的に検出してくれるからです。
また、クラッシュや脆弱性を誤って引き起こす心配なく、より大胆なコードの最適化にも自信を持って取り組むことができます。

<!--
But Rust isn’t limited to low-level systems programming. It’s expressive and
ergonomic enough to make CLI apps, web servers, and many other kinds of code
quite pleasant to write — you’ll find simple examples of both later in the
book. Working with Rust allows you to build skills that transfer from one
domain to another; you can learn Rust by writing a web app, then apply those
same skills to target your Raspberry Pi.
-->
しかし、何もRustで行えるのは低レベルのシステムプログラミングに限りません。
Rustは十分に表現力豊かで使いやすいため、CLIアプリケーションやWebサーバー、その他多くの種類のコードをとても快適に記述できます
— この本の後半には両者のシンプルな例も登場します。
Rustで作業することで、一つの分野から別の分野へと応用可能なスキルを身につけることができるのです。
例えば、Webアプリケーションを作成してRustを学び、それと同じスキルをRaspberry Piを対象としたプログラムを作成する際に適用することができます。

<!--
This book fully embraces the potential of Rust to empower its users. It’s a
friendly and approachable text intended to help you level up not just your
knowledge of Rust, but also your reach and confidence as a programmer in
general. So dive in, get ready to learn—and welcome to the Rust community!
-->
この本は、Rustがユーザーの能力を拡張することに関して、そのポテンシャルを余すことなく取り込んでいます。
Rustの知識だけでなく、プログラマーとしての幅広い能力と自信を高めるための、親しみやすくわかりやすい文書となっています。
さあ、飛び込んで、学ぶ準備をしましょう ― そして、Rustコミュニティへようこそ！

<!--
— Nicholas Matsakis and Aaron Turon
-->
- ニコラス・マットサキス(Nicholas Matsakis)とアーロン・チューロン(Aaron Turon)
