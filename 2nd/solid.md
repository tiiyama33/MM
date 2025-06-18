<h2>固体の構造を描く</h2>
<h3>結晶の単位格子を描く</h3>
固体のうち、「結晶」は原子が規則正しく並んだ構造を持っています。VESTA を使ってその構造を描きます。
<blockquote>固体は、原子の並び方によって「結晶」(crystal)と「アモルファス」(amorphous, 非晶質ともいう)の二つに大別されます。
「結晶」では原子が規則正しく並んでおり、ダイヤモンドや、鉄や銀などの金属がこれにあたります。
「アモルファス」では原子の配列は乱れており、長距離にわたる秩序性を持ちません。ガラスやプラスチックがこれにあたります。
この授業では、「結晶」について取り扱います。</blockquote>
「結晶」の構造は「単位格子」の 3 次元的な繰り返しとして表現できます。高校の授業で出てきたような「単位格子」の模型図をまず描いてみましょう。

後々のために、できるだけ繰り返して使えるようなシートを作ります。体心立方格子を例として説明します。

[caption id="attachment_3312" align="alignnone" width="794"]<img class="size-full wp-image-3312 " title="iron" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/iron.png" alt="" width="794" height="492" /> 体心立方格子の座標を計算するためのワークシート[/caption]

上図のように、緑色の部分に<span style="color: #009900;">単位格子の各方向の辺の長さ</span>を、青色の部分に<span style="color: #0000ff;">単位格子の辺の長さを 1 とした原子の <em>xyz</em> 座標</span>をそれぞれ入力すれば、赤色の部分に <span style="color: #ff0000;">xyz ファイルに入力する原子の座標</span>が表示されるようなシートを作ります。
こうすることで、異なる構造を計算する場合にも、緑や青の部分を入力するだけで済みます。

赤色の座標の部分は、緑や青の部分を参照し、計算するようにします。たとえば、上の <span style="color: #ff0000;">I8 セル(8 行目の I 列目のセル)</span>は、<span style="color: #009900;">単位格子の <em>x</em> 方向の大きさ(I4)</span>と、<span style="color: #0000ff;"><em>x</em> 座標(D8)</span>のかけ算です。従って=<span style="color: #009900;">I4</span>*<span style="color: #0000ff;">D8 </span>と書けます。
さらに、コピー時に緑色部分の<strong>行</strong>が移動しないように $ (ダラー)を挿入して =I<strong>$</strong>4*D8 としておけば、I8 セルを「コピー」し、座標を示す部分全体(I8～K16)に「ペースト」することで一気に赤い部分の計算ができます。　($ の位置には意味があります。 I$4 と書けばコピーの時に行(4)が固定、 $I4 と書けば列(I)が固定、 $I$4 と書けば行も列も固定されます。)

ついでですが、原子の数を入力する H6 セルには、 =countif(H8:H1000,"*") と入力しておけば、原子の数が自動的に入力されます。(エクセルの countif のヘルプを参照してください。)

近い将来、実験データをエクセル等で解析する際に、繰り返し使えるようなわかりやすいシートを作成することが必要になってきます。今回の授業で作成するエクセルシートも使い捨てにせず、途中の段階もそれぞれ識別しやすい名前をつけ保存しておきましょう(例えば 鉄-単位格子.xls 、金-単位格子.xls など)。この後の問題で使えるかもしれません。

[help]
<h4><strong>問題 6</strong> (鉄と金の単位格子)</h4>
(1) 鉄(Fe)の単位格子は体心立方格子(body centered cubic)であり、その一辺は 2.867 Å である。鉄の単位格子を図示せよ。また最隣接原子の数と、距離を答えよ。

(2) 金(Au)の単位格子は面心立方格子(face centered cubic)であり、その一辺は 4.070 Å である。金の単位格子を図示せよ。また最隣接原子の数と、距離を答えよ。

原子の大きさとしては原子半径([Atomic])を使うのが適切です。
原子同士がちょうど接触していることを確かめてください。

原子の間に線を引きたい場合、<a title="原子間にひく線の設定" href="http://science.shinshu-u.ac.jp/~tiiyama/?page_id=3246">「結合」の設定</a>を行ってください。

原子半径
Fe 1.26 Å
Au 1.44 Å
(VESTA中にすでに設定されています。)

[/help]

[help]
<h4><strong>問題 7</strong> (塩の単位格子)</h4>
(1) 塩化ナトリウム(NaCl)の単位格子を図示せよ。NaCl は塩化ナトリウム型と呼ばれる単位格子を持ち、その一辺は 5.628 Å である。

(2) 塩化カリウム(KCl)の単位格子を図示せよ。KCl も塩化ナトリウム型の単位格子を持ち、その一辺は 6.293 Å である。

[caption id="attachment_3313" align="alignnone" width="253"]<img class="size-full wp-image-3313 " title="NaCl" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/NaCl.png" alt="" width="253" height="231" /> 塩化ナトリウム型の単位格子 (注 上の図全体で、ひとつの単位格子です！)　(「分子・固体の結合と構造」、David Pettifor著、青木正人、西谷滋人訳、技報堂出版)[/caption]

これらの結晶の中では原子はイオン化しているので、イオン半径([Ionic])を使って書くのが適切です。

イオン半径
Na<sup>+</sup> 1.02 Å
K<sup>+</sup> 1.51 Å
Cl<sup>-</sup> 1.81 Å
これらはそれぞれのイオンの 6 配位時のイオン半径です(VESTA中にすでに設定されています)。上記の構造をイオン半径を使って描写すると、陽イオンと陰イオンが接触することを確かめてください。
なお、xyz ファイル中の元素記号としては Na や Cl と書いた方が良いようです。Na+ や Cl- と書くと、半径として異なった値が使われます。
(※どちらが Cl イオン? 脚注参照→ ((黒丸と白丸のどちらが Na か Cl かがわからない、という質問をよく受けるのですが、<strong>実はどちらでもよいのです。</strong> このあと見るように、実際の塩(NaCl)の結晶は、Na<sup>+ </sup>と Cl<sup>-</sup> が交互にえんえんと並んでいます。<strong>繰り返し単位</strong>としては、Na<sup>+ </sup>がはじっこになるようにしても、Cl<sup>-</sup> がはじっこになるようにしても、同じように結晶全体の構造を表すことができます。)) )

[/help]

<hr style="width: 650px;" />

<h3>広い範囲の結晶構造を描く</h3>
結晶は、単位格子を 3 次元的に無数に繰り返した構造を持っています。
ここではエクセル上で単位格子を何度か繰り返し、より広い範囲の結晶構造を表す方法について考えます。 <a name="repeat"></a>

[caption id="attachment_3315" align="alignnone" width="400"]<img class="size-full wp-image-3315 " title="repeat3" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/repeat3.png" alt="" width="400" height="327" /> 単位格子の繰り返し[/caption]

上の図の水色部分で示されている単位格子に含まれる原子を、単位格子の辺の方向に沿って平行移動してファイルに加えていけば、より広い範囲の原子の座標が計算されます。
上図は各方向に単位格子を 3 回ずつ繰り返した例で、元の単位格子を含み、計 27 回(3 × 3 × 3 回)単位格子が繰り返されています。

礼として、鉄(体心立方格子)について、エクセルを用いて各方向に2回づつ、合計で単位格子8個分(原子16個分)の計算をしたワークシートを下記に示します。

下記の説明を参考に、下の問題 8 を行ってください。

<a href="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2018/07/q8-nn0.png"><img class="alignnone size-full wp-image-11749" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2018/07/q8-nn0.png" alt="" width="709" height="580" /></a>

前のワークシートに、<span style="color: #ff8000;">単位格子の平行移動</span>を行うオレンジの部分が加わっています。
鉄の単位格子(体心立方格子)に含まれる鉄の原子数は 2 個です。最初の 2 行(8 行目、9 行目)は、元の単位格子に含まれる鉄原子を示しています。この 2 行ではオレンジの部分は(0, 0, 0)になっています。
次の 2 行(10 行目、11 行目))は、単位格子を <em>x </em>軸の方向に平行移動しています。この 2 行はオレンジの部分は(1, 0, 0)になっています。
つまり、オレンジの部分は、<span style="color: #ff8000;">単位格子の辺の長さを 1 とした原子の移動距離</span>を表しています。

各原子の座標(赤色の部分, 例えばI8)は次のように計算できます。
{ (<span style="color: #ff8000;">単位格子の平行移動の <em>x </em>部分 A8</span>) + (<span style="color: #0000ff;">単位格子の中の座標の <em>x</em> 部分 D8</span>) } × (<span style="color: #009900;">単位格子の <em>x</em> 方向の辺の長さ I4</span>)
$マークをうまく使えば、座標部分は 単純なコピー &amp; ペーストで済みます。
また、青色部分などは繰り返しが多いので、ここもコピー &amp; ペーストを活用しましょう。

単位格子に含まれる原子の数に注意してください。問題 6 のように体心立方格子の単位格子ひとつを図示するときは、通常各頂点に 1 個と、立方体の中心に 1 個の計 9 個の原子が描かれます。しかし、高校で習ったように、1 つの体心立方格子に実際に含まれる原子の数は 2 個です。従って、ここでは 2 個の原子についてのみ平行移動の計算を行います。

2 次元で例を挙げます。下記のような結晶があるとき、

<img class="alignnone size-full wp-image-3317" title="repeat2d" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/repeat2d.png" alt="" width="341" height="254" />

単位格子を<img class="alignnone size-full wp-image-3318" title="cell1" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/cell1.png" alt="" width="101" height="101" />とすると、単位格子に含まれる原子数は2であり、
上記の結晶は例えば<img class="alignnone size-full wp-image-3319" title="cell2" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/cell2.png" alt="" width="101" height="101" />の繰り返しで表すことができます。
<img class="alignnone size-full wp-image-3320" title="cell3" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/cell3.png" alt="" width="101" height="101" />の繰り返しをすると、原子が重複してしまいます。

<a title="問題 8 のヒント" href="http://science.shinshu-u.ac.jp/~tiiyama/?page_id=3323">もう少し詳しい説明</a>(←クリック！)

[help]

<a name="q8"></a>
<h4><strong>問題 8</strong> (単位格子を繰り返す)</h4>
<ol type="i">
 	<li>鉄の結晶について、単位格子を<em>x</em>, <em>y</em>, <em>z</em> の各方向に 2 ~ 3 回以上繰り返してその全体を図示せよ。
(全体像が立方体になるように繰り返す)</li>
 	<li>また、問題 6, 7 で書いた単位格子から一つ(鉄以外)を選び、同様に広い範囲の結晶構造を図示せよ。</li>
</ol>
よくわからない人は<a title="問題 8 のヒント" href="http://science.shinshu-u.ac.jp/~tiiyama/?page_id=3323">もう少し詳しい説明</a>を参照しながら進めてください。
[/help]

(注 問題 6 で答えた「最隣接原子の数」は、繰り返しの分をきちんと考えましたか？)
