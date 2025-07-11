>[!note]
>このページから、[問題]がでてきます。問題の解答はレポートに記載し、提出してもらいます。  
>レポートを作りながら作業を進めていくとよいでしょう。  
>(「<a title="レポートについて(情報科学演習)" href="/docs/report.md">レポートについて</a>」のページに、レポートのテンプレート(雛形; ひながた) があります。)

# VESTA の使い方
うまく起動できたら、下記のような画面が表示されるはずです。
このソフトウェアVESTAを使って分子を表示していきます。
(表示はすべて英語ですが、くじけずに頑張ってください。)

<figure>
  <img src="/img/window1.png" alt="" width="557" height="475"/>
  <figcaption>VESTAの画面</figcaption>
</figure>

## 分子データの読み込み
さっそく分子を表示させてみることにしましょう。  

下にエタノールの座標ファイルを置きました。ダウンロードしてください。

[ethanol.xyz](/files/ethanol.xyz)
  
上記リンクを左クリックするとethanol.xyzの内容が表示されるので、  
上部の ダウンロードボタン(download raw file) <img src="/img/download.png" width="30"> を押してください。  
> ファイルは[ダウンロード]フォルダに保存されます(Chromeの場合)

保存したethanol.xyz ファイルを、VESTA(上の図中G)に Drag & Drop してみましょう。
> または VESTAのメニュー(上の図中A)中の[File]-[Open...]からファイル ethanol.xyz を開いてもOK

球と棒で示されたエタノール分子が表示されたでしょうか？

**分子はマウス操作(上図Gで左ボタンをドラッグ(押したまま動かす))で回転させることができます。** 試してみてください。

> 回転しない場合は左メニューで **[回転]モード** <img class="alignnone size-full wp-image-6430" src="/img/rotate1.png" alt="rotate" width="30"/> が選ばれていることを確認してください。

> 初期設定では、平行法(Parallel; 遠くのものも小さくしない)で分子を描いているので、回転が不自然に感じるかもしれません。  
> メニュー(上図A) [View] (視点)から **[Perspective]** (遠近法)を選択すると、遠くの分子を小さく描き、遠近感のある描写になります。
> (xyzファイルを読み込むたびに行う必要がある。)

> [O-H間に引かれている点線を消す](/tips/ethbond.md)

## 分子の操作
動作モードは [Manipulation] (上図E)で切り替えます。

<table border="0">
<tbody>
<tr>
<td><img class="alignnone size-full wp-image-6430" src="/img/rotate1.png" alt="rotate" width="70" height="64" /></a></td>
<td>[Rotate]
(回転)</td>
<td>分子をマウス操作で回転します。</td>
</tr>
<tr align="left" valign="middle">
<td><img class="alignnone size-full wp-image-6432" src="/img/select1.png" alt="select" width="70" height="64" /></a></td>
<td>[Select]
(選択)</td>
<td>原子を選択します。
原子の情報(元素名、座標など)が情報ウィンドウ(上図H)に表示されます。</td>
</tr>
<tr align="left" valign="middle">
<td><img class="alignnone size-full wp-image-6433" src="/img/translate1.png" alt="translate" width="70" height="64" /></a></td>
<td>[Translate]
(並進)</td>
<td>マウス操作で分子の表示位置を変更します。</td>
</tr>
<tr align="left" valign="middle">
<td><img class="alignnone size-full wp-image-6434" src="/img/magnify1.png" alt="magnify" width="70" height="64" /></a></td>
<td>[Magnify]
(拡大)</td>
<td>マウス操作で視点を近づけたり遠ざけたりすることで、分子を拡大、縮小します。マウスのホイールでも代用可能。</td>
</tr>
<tr align="left" valign="middle">
<td><img class="alignnone size-full wp-image-6435" src="/img/distance1.png" alt="distance" width="70" height="64" /></a></td>
<td>[Distance]
(距離)</td>
<td>2つの原子を続けて選択することで、その原子間の距離を情報ウィンドウ(上図H)に表示します。</td>
</tr>
<tr align="left" valign="middle">
<td><img class="alignnone size-full wp-image-6436" src="/img/angle1.png" alt="angle" width="70" height="64" /></a></td>
<td>[Angle]
(角度)</td>
<td>3つの原子を続けて選択(a-b-c)することで、その角度を情報ウィンドウ(上図H)に表示します。</td>
</tr>
<tr align="left" valign="middle">
<td><img class="alignnone size-full wp-image-6437" src="/img/dihedral1.png" alt="dihedral" width="70" height="64" /></a></td>
<td>[Dihedral]
(二面角)</td>
<td>相交わる二平面のなす角を情報ウィンドウ(上図H)に表示します。</td>
</tr>
</tbody>
</table>

>[!important]
> ### 問題 1 エタノール分子のかたち
> (問題の解答は、レポートに記載してください。)
>
>(1) エタノール分子の、C-C-O の角度は何度か (原子を選ぶ順番に注意)
>
>(2) エタノール分子の O-H 間距離、C-H 間距離 (隣接しているもの)は何オングストロームか
>
>有効数字は小数点以下 2 桁とする。

>一部のノートパソコンでは、原子を選択できない、というバグが生じるようです。  
>(2)の原子距離については、  
>ball & stick モデルで表示している状態で、画面左アイコンの上から2番目、[選択] <img src="/img/select1.png"> モードにして、結合部分を選ぶと、その距離が表示される
>という方法で代用することができます。

>[!note]
>オングストローム(Å; Aの上に丸)は長さの単位で、1 Å = 10<sup>-10</sup> m です(1 Å = 0.1 nm = 100 pm)。  
>国際単位(SI単位)ではないので現在は使わないことになっていますが、原子の大きさを表すのに便利 (水素原子の直径が約 2 Å) なので、このソフトウェアをはじめ、一部でまだ利用されています。

>Å (オングストローム) や ° (度) は全角文字(日本語フォント)にも用意されていますが、数字に並べて使うとバランスがいまいちです。  
>ワードでは、下記のような方法で、半角(欧文フォント)の Å  や ° を入力できます。
> - [Åの入力] [挿入]-[記号と特殊文字]-[ラテン1補助]から選んで入力する
> - [Åの入力] 半角入力モードで Ctrl+@(同時押し)に続けて Shift+A(同時押し)を押す。
> - [Åの入力] ワードの数式エディタで A ¥above ¥circ と入力してもよい。
> - [° の入力] 半角入力モードでかつ欧文フォントが選ばれている状態で Ctrl+@につづけてスペースを押す。
> - [° の入力] 数式エディタで ¥degree と入力する
> - [äの入力] 他にも例えば Ctrl+: に続けて a を押すと ä が入力できる。


[前＜](install.md) [目次](/README.md) [＞次](molecule.md)
