# VESTAのその他の項目

<h2>表示方法を変えたときの例(アデニン)</h2>
<div>

<span class="Apple-style-span"><a title="受講生用ページ" href="http://science.shinshu-u.ac.jp/~tiiyama/?page_id=3194">アデニン</a>を例として、表示法を変えたときの分子像を示します。
</span>

[caption id="attachment_6584" align="alignnone" width="300"]<a href="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/Adenine-bs.png"><img class="wp-image-6584 size-medium" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/Adenine-bs-300x227.png" alt="Ball-and-Stick 市販の分子模型のような表示です。" width="300" height="227" /></a> Ball-and-Stick<br />市販の分子模型のような表示です。分子の結合の様子を知るのに適しています。[/caption]

[caption id="attachment_6585" align="alignnone" width="300"]<a href="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/Adenine-vw.png"><img class="wp-image-6585 size-medium" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/Adenine-vw-300x227.png" alt="Space-filling(van der Waals半径使用) 分子の実際の形を知るのに適しています。" width="300" height="227" /></a> Space-filling(van der Waals半径使用)<br />van der Waals 半径は、分子を構成した時の電子雲の広がりに概ね対応しています。分子の実際の形を知るのに適しています。[/caption]

[caption id="attachment_8298" align="alignnone" width="300"]<a href="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2013/06/Adenine-atom.png"><img class="wp-image-8298 size-medium" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2013/06/Adenine-atom-300x207.png" alt="Space-filling(Atomic)" width="300" height="207" /></a> Space-filling(原子半径(Atomic)使用) <br />原子半径は固体結晶中の結合距離の半分が設定されています。後で行う固体結晶の構造を描くときには有用ですが、エタノールやアデニンのような「分子」を描く際にはあまり意味がありません。[/caption]

[caption id="attachment_6586" align="alignnone" width="300"]<a href="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/Adenine-wf.png"><img class="wp-image-6586 size-medium" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/Adenine-wf-300x227.png" alt="Wireframe(ワイヤーフレーム) タンパク質等の大きな分子を表示するのに適しています。" width="300" height="227" /></a> Wireframe(ワイヤーフレーム)<br />タンパク質等の大きな分子を表示するのに適しています。[/caption]

[caption id="attachment_6587" align="alignnone" width="300"]<a href="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/Adenine-st.png"><img class="wp-image-6587 size-medium" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/Adenine-st-300x227.png" alt="Stick 分子間の結合のみを示します。分子結合に注目する際に使います。" width="300" height="227" /></a> Stick<br />分子間の結合のみを示します。分子結合に注目する際に使います。[/caption]

<hr />

</div>
<h2>表示方法の変更</h2>
VESTAの他の設定項目の説明です。

[caption id="attachment_3191" align="alignleft" width="557"]<a href="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/window.png"><img class="size-full wp-image-3191" src="http://science.shinshu-u.ac.jp/~tiiyama/wp-content/uploads/2011/07/window.png" alt="VESTAの画面" width="557" height="475" /></a> VESTAの画面[/caption]

<hr style="width: 650px;" />

<h2></h2>
分子の表示方法は[Structural Model](上図C)で切り替えることができます。
<ul>
 	<li>[Ball and Stick] 球と棒のモデル
初期設定です。球の直径は、実際の原子の大きさよりもかなり小さい値が設定されています。</li>
 	<li><strong>[Space-filling] 空間充填モデル</strong>
エタノールのような小さな分子の形状を知るためには最も有用です。
表示される原子の直径は次の方法で切り替えます。
<ol>
 	<li>[Properties]ボタン(上図D)を押す。</li>
 	<li>[Atoms]タグを選択。</li>
 	<li>[Atom style]-[Show as balls]でRadii Type(直径のタイプ)を切り替える
<ul>
 	<li>[Atomic] 原子半径
同種原子が作る化学結合距離の半分の値が半径として設定されています。</li>
 	<li>[Ionic] イオン半径
イオンとなったときの半径が設定されています。(C や O は通常イオン化していないので、エタノールではあまり意味がない)</li>
 	<li><strong>[van der Waals] ファンデルワールス半径</strong>
ファンデルワールス半径を使って分子が描かれます。</li>
</ul>
表示される原子の半径(Radius)や色は、必要があれば画面下の[Radius and color]で原子種を選択して設定することができます。(色は左からRed、Green、Blue(光の 3 原色)を 256 段階で表している。)

原子は多角形の回転体として表示されているので、[Resolution]の値(Stacks, Slices 両方)を(60くらいに)大きくすると、つるつるの球として表示されます。(やりすぎると表示に時間がかかります)</li>
</ol>
</li>
 	<li>[Polyhedoral] 多面体
結晶構造に含まれる SiO<sub>4</sub> を正四面体として表示します。最初にでてきたゼオライトはこれを使って表示しました。<a title="空間群を利用して、さらに複雑な構造を描く" href="http://science.shinshu-u.ac.jp/~tiiyama/?page_id=3434">問題14</a> ででてきます。</li>
 	<li>[Wire-flame]
ワイヤーフレーム 原子間結合をワイヤーで表現します。</li>
 	<li>[Stick] 棒
原子間の結合を棒で表現します。</li>
 	<li>[Show dot surface]
点で表面を表示 [Space-filling]で設定された球の表面を点で表現します。</li>
</ul>
<h2>その他の情報</h2>
視点の変更は、メニューバー(上図 B)からも行うことができます。
<ul>
 	<li>[ a ],[ b ],[ c ],[ a* ],[ b* ],[ c* ] それぞれ、 <em>x</em> 軸方向から、<em>y</em> 軸方向から、<em>z</em> 軸方向から分子を見ます。
(a* ボタンは、今のところ a ボタンと同じ働きをします。)</li>
 	<li>△矢印 6 つ 視点に平行、垂直な方向に、指定された角度だけ分子を回転します。
1 回押すと決まった角度だけ動くので、特定の角度から(側面図など)図を描く場合に便利です。</li>
 	<li>[↑], [↓], [←], [→] 指定されたピクセル(画素)数だけ、分子を平行移動します。</li>
 	<li>[+], [-], [ ] それぞれ、分子を拡大(視点を近づける)、縮小(視点を遠ざける)、分子が画面いっぱいになるよう調整、します。</li>
</ul>
<ul>
 	<li>上図 F の [Drag] を [Animation] に切り替えると、分子模型が自動で回転します。(止めるときは [Drag] に戻す。)</li>
 	<li>[Ball-and-Stick] で、原子と原子の間に引かれる「結合」は<a title="原子間にひく線の設定" href="http://science.shinshu-u.ac.jp/~tiiyama/?page_id=3246">[Edit]-[Bonds...]から設定します</a>。(あとでまたやります。)</li>
 	<li>[View] から、他にも表示に関するいろいろな設定ができます。
<ul>
 	<li>[Antialiasing] アンチエイリアシング 分子の縁の部分のぎざぎざをなめらかにする。通常ON。</li>
 	<li>[Parallel] 平行法で分子を描く。近くの原子も遠くの原子も同じ大きさで描かれる。</li>
 	<li>[Perspective] 遠近法で分子を描く。遠くの分子は小さく描かれる。</li>
 	<li>[Overall Appearance...] その他の設定
<ul>
 	<li>Background color 背景の色の設定</li>
 	<li>Light 光源の設定</li>
 	<li>Projection 視点の距離の設定</li>
 	<li>Depth-cueing 遠くの分子の色を薄く表示する機能の設定</li>
</ul>
</li>
</ul>
</li>
 	<li>2 つ以上のファイルを開いた場合は、G の上に現れるタブでファイルを切り替えます。</li>
</ul>
<div>
