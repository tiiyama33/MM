<h2>分子の座標ファイルを作成する</h2>
<h3>エディタを使って座標ファイルを作る</h3>
VESTA が表示する分子の構造(原子の位置)は、座標ファイルの中に書かれています。
先ほど使った、エタノール分子の座標ファイル ethanol.xyz の中(実体)を見てみましょう。

実体を見るためには [エディタ] と呼ばれるソフトウェアを使います。
この授業では [メモ帳] (NotePad)を使います (([メモ帳] は Windows 標準添付のソフトウェアです。)) (Macの人は脚注参照→ ((Mac OS Xの場合、標準で搭載されている[テキストエディタ]が使えます。起動時は[リッチテキスト]モードになっているので、[テキストエディット]-[環境設定...]-[フォーマット]で [標準テキスト]モードに切り替えてください。拡張子(ファイル名の最後の部分)は強制的に .txt となってしまうので、ファイルをセーブした後、ファイル名末尾を .xyz に直してください。 )) )。

[メモ帳] は [スタートメニュー]-[Windowsアクセサリ]-[メモ帳] あたりにあると思います。(場所が違う可能性あり)
<ol>
 	<li>画面左下の[スタートボタン]を押し、[Windows アクセサリ] の中の[メモ帳]をクリック

[caption id="attachment_195899" align="alignnone" width="288"]<a href="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2021/06/memo.png"><img class="size-medium wp-image-195899" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2021/06/memo-288x300.png" alt="" width="288" height="300" /></a> メモ帳[/caption]</li>
</ol>
ダウンロードした ethanol.xyz を、起動した [メモ帳] に Drag &amp; Drop、または [ファイル]-[開く] で 開いてください。

[caption id="attachment_8165" align="alignnone" width="300"]<a href="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/notepad1.png"><img class="wp-image-8165 size-medium" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/notepad1-300x281.png" alt="ＮotePadでethanol.xyzを開いたところ" width="300" height="281" /></a> [メモ帳] で ethanol.xyzを開いたところ[/caption]ethanol.xyz は "XMol XYZ" 形式に従って書かれています。
(ファイルの拡張子は .xyz )

"XMol XYZ" 形式は分子の情報を以下のように書くように定められています。
<ul>
 	<li>1 行目 原子の個数を書く</li>
 	<li>2 行目 分子の名称を書く(日本語禁止)</li>
 	<li>3 行目以降
1 行が 1 つの原子の情報を表している。それぞれの行には各原子の
元素記号 <em>x</em> 座標 <em>y</em> 座標 <em>z</em> 座標
を書く。<strong>座標は Å (オングストローム) 単位 </strong> ((1 Å = 10<sup>-10</sup> m ))<strong>。 元素記号と各座標の間はスペースで区切る。</strong>
(スペースの数は何個でも良い。ただし、全角スペースは使わないこと。タブ(Tab) も区切りに使えるが、タブの場合は 2 個以上連続して並べてはいけない。)</li>
</ul>
つまり、原子の座標を調べ、上のようなフォーマットで 拡張子を .xyz としたファイルを作れば、どのような分子でも図に描くことができます。

[help]
<h4><strong>問題 4</strong> (メタン)</h4>
下記の座標を利用してメタン分子の座標ファイルを作成し、それを使ってメタンの分子模型を図示せよ。またVESTAを用いてメタン分子のH-C-H結合角を求めよ。

[/help]

[caption id="attachment_3266" align="alignnone" width="600"]<img class="size-full wp-image-3266 " title="methane" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/methane.jpg" alt="" width="600" height="267" /> メタン分子の原子座標[/caption]

[メモ帳] で、[ファイル]-[新規] を選んで新しいファイルを開き、"XMol XYZ" 形式に従って上記の座標を入力します。以下の点に注意してください。
<ul>
 	<li>ファイルの中では全角文字は使わない。</li>
 	<li>1行目は原子数を入力</li>
 	<li>2行目は分子名(methane または CH4) を入力</li>
 	<li>3行目以降は、元素名、xyz座標をスペースで区切り入力</li>
</ul>
座標データが入力できたら、ファイルの種類を <strong>[すべてのファイル]</strong> に変更して、methane.xyz という名前でセーブしてください。((NotePad++ の場合、ファイルの種類は[Normal text file (*.txt)] のままでよいようです。))
<a href="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/save1.png"><img class="alignnone size-medium wp-image-8166" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/save1-300x200.png" alt="save1" width="300" height="200" /></a>
(ファイルの種類を [テキストファイル] のままでセーブすると、ファイル名が methane.xyz.txt となってしまうようです。その場合、できたファイルの名前を変更して最後の .txt を消してください。)

うまく入力できていれば、作ったファイル(methane.xyz) を VESTA で開くとメタンの分子模型が表示されるはずです。
<blockquote>1カ所でも間違いがあると、VESTAで開いたときに、VESTAがエラーを出して強制終了してしまうことがあります。その場合はよくファイルの内容を見直してください。

間違いの例
<ul>
 	<li>1行目の原子数が違っていた</li>
 	<li>2行目が抜けていた</li>
 	<li>数値の小数点がカンマになっていた</li>
 	<li>区切りのスペースが抜けていた</li>
 	<li>スペースや数字に全角文字を使っていた</li>
 	<li>1つの数値に小数点を2回使っていた</li>
 	<li>小数点をつけるのを忘れて、ものすごく遠いところに原子を描いていた　など</li>
</ul>
</blockquote>

<hr style="width: 650px;" />

<h3>エクセルを使って座標を計算する</h3>
次に、水分子とベンゼン分子を描いてみましょう。ただし、原子の位置は自分で計算してもらいます。
次の問題 5 を行ってください。

[help]
<h4><strong>問題 5</strong> (水、ベンゼン)</h4>
(1) 水蒸気の赤外、ラマンスペクトルの研究によると、
水分子の O-H 結合距離は 0.9575 Å、H-O-H 結合角は 104.31° である。
水分子の構造モデルを図示せよ。

(2) 同じく、ベンゼン分子 (C<sub>6</sub>H<sub>6</sub>) の C-C 結合距離は 1.397 Å、C-H 結合距離は 1.076 Å である。ベンゼン分子の構造モデルを図示せよ。
(どこを原点(<em>x</em> = 0, <em>y</em> = 0, <em>z</em> = 0)にすれば計算が楽か、よく考えてください。必ずしも原点に原子がある必要はありません。)

[/help]

座標計算は、エクセルを使って行います。
次の方法で、エクセルを使って xyz ファイルに入力するデータを作成することができます。

[caption id="attachment_3269" align="alignnone" width="630"]<img class="size-full wp-image-3269 " title="excel" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/excel.png" alt="" width="630" height="425" /> エクセルで座標を並べたところ (例はメタン分子。数値は正しい値ではありません)[/caption]
<ol>
 	<li>上図のように、xyz 形式に合うように原子数や元素名、座標をエクセルのセルに並べる (座標は三角関数を使って計算する)</li>
 	<li>上図のように、xyz 形式の部分を選択して [コピー] する</li>
 	<li>[メモ帳] を立ち上げ新しいファイルを開く
(すでにファイルが開かれているときは、[ファイル]-[新規作成] で新しいファイルを作成する)</li>
 	<li>[メモ帳] に [ペースト] する
([メモ帳]にペーストすると、数式ではなく答えの「数値」が貼り付けられます)</li>
 	<li>.xyz をつけたファイル名でセーブする</li>
</ol>
[caption id="attachment_3270" align="alignnone" width="511"]<img class="size-full wp-image-3270 " title="paste" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/paste.png" alt="" width="511" height="274" /> エディタにペーストしたところ[/caption]

これでエクセルから[メモ帳]にデータを移動し、.xyz ファイルを作る方法が分かりました。

各原子の座標はエクセル上で三角関数を使って計算します。
エクセルから[メモ帳]にペーストする際には、数式ではなく答えの数値が貼り付けられますので、エクセル上では例えば
<pre>=10∗sin(radians(30))</pre>
というように、直接数式を入力してかまいません。

エクセルでの三角関数の使い方を下に書いておきます。角度として <strong>ラジアン</strong> を使うことに注意してください。
水とベンゼン分子のモデルを順に作成してください。

<strong>分子模型を製作後、計算が合っているかどうか VESTA 上で原子間距離や角度を確かめてみること！</strong>

[note]
<h4>エクセルによる三角関数の計算</h4>
sin30° → = sin(30*3.14/180)
または → = sin(30*pi()/180)
または → = sin(radians(30))
(いずれも 30° をラジアンに変換してから sin に入れている)

※ pi() は円周率を返す関数。(かっこの中には何も入れない)
radians() は度をラジアンに変換する関数。
ラジアン→度の変換は degrees() で行える。
他、覚えておいて欲しい関数は
^ (ハット) 累乗 (2の3乗 → =2^3),
log() 常用対数,
ln() 自然対数,
exp() 指数関数 (eの3乗 → =exp(3) )
sqrt() ルート(ルート2→ = sqrt(2) 、=2^(1/2)でも同じ)
など。参照→<a href="http://science.shinshu-u.ac.jp/~tiiyama/?page_id=9616" target="_blank" rel="noopener noreferrer">エクセルの関数</a>　(エクセルのメニュー中の[数式]-[関数の挿入]で一覧が出てきます。)

[/note]

[help]<a name="5-2"></a>
<h4><strong>問題 5-2</strong> (炭化水素類; 余剰問題)</h4>
(余裕のある人は挑戦してください。)

次の分子を図示せよ。
<ol>
 	<li>エタン(C<sub>2</sub>H<sub>6</sub>) (ねじれ型配座が最安定)
C-C-H 結合角 109.6°、C-C 結合距離 154 pm、C-H 結合距離 110 pm</li>
 	<li>エチレン(C<sub>2</sub>H<sub>4</sub>)
C-C-H 結合角 121.7°、C-C 結合距離 133 pm、C-H 結合距離 108 pm</li>
 	<li>アセチレン(C<sub>2</sub>H<sub>2</sub>)
C-C-H 結合角 180°、C-C 結合距離 120 pm、C-H 結合距離 106 pm</li>
</ol>
1 pm (ピコメートル) = 0.01 Å
参照→接頭語

[/help]
