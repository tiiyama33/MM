# 立方体以外の単位格子の繰り返しの考え方
問題 9 (氷)
<ol type="i">
<li>下図は氷(Ice I<sub>h</sub>)の単位格子である。氷の構造を図示し、その特徴について述べよ。酸素原子のみを示せばよい。(水素原子は示さなくてよい)</li>
</ol>
<p>&nbsp;</p>
[caption id="attachment_3383" align="alignnone" width="600" caption="真上(z 軸方向) からみた氷の単位格子の繰り返し"]<img class="size-full wp-image-3383" title="ice-repeat" src="/img/ice-repeat.png" alt="" width="600" height="266" />[/caption]
<p>このような立方体以外の形の単位格子では、ベクトルの考え方を使います。</p>
<p>単位格子は 3 つのベクトル、 <strong>a</strong>, <strong>b</strong>, <strong>c</strong> で表すことができます。(以下、太字はベクトルを表しています)<br />ベクトルを次のように成分表示で書くことにすると</p>
<ul>
<li><strong>a</strong> = (a<sub>x</sub>, a<sub>y</sub>, a<sub>z</sub>)</li>
<li><strong>b</strong> = (b<sub>x</sub>, b<sub>y</sub>, b<sub>z</sub>)</li>
<li><strong>c</strong> = (c<sub>x</sub>, c<sub>y</sub>, c<sub>z</sub>)</li>
</ul>
<p>下図の氷(Ice I<sub>h</sub>)の場合、3 つのベクトルはx, y, z の成分表示で例えば次のように書けます。(他の書き方もあります)</p>
<ul>
<li><strong>a</strong> = (4.48*cos60°, 4.48*sin60°, 0)</li>
<li><strong>b</strong> = (-4.48, 0, 0)</li>
<li><strong>c </strong>= (0, 0, 7.31)</li>
</ul>
<div style="text-align: left;"><span style="font-size: small;"><span style="border-collapse: collapse; line-height: 24px;">[caption id="attachment_3367" align="alignnone" width="300" caption="氷(Ih)の単位格子"]<a href="/img/ice-s.png"><img class="size-medium wp-image-3367" title="氷(Ih)の単位格子" src="/img/ice-s-300x219.png" alt="" width="300" height="219" /></a>[/caption] [caption id="attachment_3368" align="alignnone" width="260" caption="横から見たところ(数字は長さの比)"]<a href="/img/ice-ss.png"><img class="size-medium wp-image-3368" title="横から見たところ(数字は長さの比)" src="/img/ice-ss-260x300.png" alt="" width="260" height="300" /></a>[/caption] [caption id="attachment_3375" align="alignnone" width="300" caption="上から見たところ(数字は長さの比)"]<a href="/img/ice-st.png"><img class="size-medium wp-image-3375" title="上から見たところ(数字は長さの比)" src="/img/ice-st-300x187.png" alt="" width="300" height="187" /></a>[/caption]<br /></span></span></div>
<p>そうすると、単位格子に含まれる 4 つの酸素原子の位置は、3 つのベクトル<strong>a</strong>, <strong>b</strong>, <strong>c </strong>を使って次のように書けます。</p>
<ul>
<li><strong>O<sub>1</sub></strong> = (1/3)*<strong>a</strong>+(2/3)*<strong>b</strong>+(1/16)*<strong>c</strong></li>
<li><strong>O<sub>2</sub></strong> = (1/3)*<strong>a</strong>+(2/3)*<strong>b</strong>+(7/16)*<strong>c</strong></li>
<li><strong>O<sub>3</sub></strong> = (2/3)*<strong>a</strong>+(1/3)*<strong>b</strong>+(9/16)*<strong>c</strong></li>
<li><strong>O<sub>4</sub></strong> = (2/3)*<strong>a</strong>+(1/3)*<strong>b</strong>+(15/16)*<strong>c</strong></li>
</ul>
<p>実際の xyz ファイルには各酸素原子の xyz 座標を書く必要があります。<br />O<sub>1 </sub>の x 座標は、上の式の <strong>a</strong>, <strong>b</strong>, <strong>c</strong> の x 成分をとりだして計算すればよいので、以下のように計算できます。</p>
<ul>
<li>O<sub>1x</sub> = (1/3)*a<sub>x</sub> + (2/3)*b<sub>x</sub> + (1/16)*c<sub>x</sub></li>
<li>すなわち</li>
<li>O<sub>1x</sub> = (1/3)*(4.48*cos60°) + (2/3)*(-4.48) + (1/16)*0</li>
</ul>
<p>同じように、y 座標と z 座標も求めることができます。</p>
<ul>
<li>O<sub>1y</sub> = (1/3)*a<sub>y</sub> + (2/3)*b<sub>y</sub> + (1/16)*c<sub>y</sub></li>
<li>O<sub>1z</sub> = (1/3)*a<sub>z</sub> + (2/3)*b<sub>z</sub> + (1/16)*c<sub>z</sub></li>
</ul>
<p>うまくセルを並べて、$マークを駆使すれば、計算は一気に行えます。</p>
<p><a href="http://dione.shinshu-u.ac.jp/iiyama/jyouhou/ice-excel2.png"></a><a href="/img/ice-excel1.png"><img class="alignnone size-full wp-image-3386" title="ice-excel" src="/img/ice-excel1.png" alt="" width="794" height="456" /></a><a href="/img/ice-excel2.png">赤い部分の答え</a>(やり方は他にもあります。)</p>
<blockquote>
<p>上の表で 2.22045E-16 とあるのはコンピュータの世界で指数形式と呼ばれるもので、<br />2.22045 × 10<sup>-16</sup> を表しています。つまりこの場合、ほぼ 0です。<br />VESTAはこの指数形式も読み込むことができるので、そのまま xyz ファイルに貼り付けてかまいません。<br />表示の違いが気になる場合は、セルを選択して、エクセル上のメニューから[書式]-[セル]で表示される[セルの書式設定]で表示形式を[標準]から[数値]に変更し、[小数点以下の桁数]を 3 桁程度に設定してやるとよいでしょう。設定の桁数になるように四捨五入され、表示されます。<br />この設定は、将来書く実験のレポートで、数値を有効数字の桁に揃えるときに使います。</p>
</blockquote>
<p><a title="発展問題" href="http://science.shinshu-u.ac.jp/~tiiyama/?page_id=3359#q9hint">[問題 9 に戻る]</a></p>
