# 空間群を利用して、さらに複雑な構造を描く (Q14のヒント)

>[!important]
>### 問題 14 ゼオライト
>ゼオライトの結晶構造をひとつ選び、構造を図示してその特徴について述べよ。
>(物質名を示すこと。)

最後に、VESTAの本来の機能を利用して、より複雑な構造を描いてみましょう。

ここでは結晶物質のひとつである、ゼオライトを題材とします。

>[!note]
>ゼオライトとは
>多孔質アルミノケイ酸塩の総称。
>四面体構造を持つ SiO<sub>4 </sub>と AlO<sub>4 </sub>が組み合わされた基本構造を持つ結晶であり、<strong>0.4~0.8 nm 程度の孔(細孔)</strong>を有している。  
>天然にも存在するが、石油精製や触媒担体として利用するために、様々な構造をもった物質が合成されている。  
>沸石とも呼ばれるが、実験で使う沸騰石とは別のもの。  


|<img title="Mordenite" src="/img/Mordenite.png" alt="" width="400" />|
|:---:|
|ゼオライトの一種、モルデナイト(Mordenite)の結晶構造|

これまでエクセルを用いて結晶内の原子の位置を計算してきましたが、結晶の対称性を利用すると、より簡単に結晶内の原子の位置を表すことができます。

<span style="font-size: small;"><span class="Apple-style-span" style="line-height: 20px;"> </span></span>

1. 現在までに構造が明らかとなったゼオライトの構造データはインターネットで公開されています。  
下記ページを開いてください。  
http://www.iza-structure.org/databases/  
**注意！</strong> ページ内の[Edit Data]ボタンを押さないでください。データベースの元データを消してしまうおそれがあります。**  
2. ページ上部のタグから [All Codes] を選びます。
3. ゼオライトはアルファベット3文字の構造コードで分類されています。  
いずれかひとつの構造コードをクリックします。(上の構造では、MORを選択)
4. 画面上部[XPD]をクリックします。  
(構造コードが同じ複数の物質が存在している場合には、そのリストが現れます。その場合にはいずれかひとつの物質名(Material Name)をクリックします。)
5. 切り替わった画面下部の [Crystal Data] (結晶データ) と書いてある部分が、結晶中の原子位置の情報です。
必要なデータは、以下の通りです。

<table border="1">
<tbody>
<tr>
<td>ページ内の記述</td>
<td>日本語</td>
<td>モルデナイトの場合</td>
<td>備考</td>
</tr>
<tr>
<td>Material Name</td>
<td>物質名</td>
<td>Mordenite</td>
<td>ページの上部に、Powder Diffraction Pattern for <strong>Mordenite</strong> のように書いてある。</td>
</tr>
<tr>
<td>Space group</td>
<td>空間群</td>
<td valign="top" height="18">Cmcm (#63)
Setting: (なし)</td>
<td>原子配置の対称性を表す記号。
3 次元の対称性は230 種に分類されることが知られており、それぞれ番号がついている。
(空間群については大木先生の授業、「固体化学」で詳しく学びます。)</td>
</tr>
<tr>
<td>Cell parameters</td>
<td>セル定数</td>
<td>a = 18.11 Å b = 20.53 Å c = 7.528 Å
α = 90° β = 90° γ = 90°</td>
<td>単位格子(結晶の繰り返し単位)の辺の長さと角度。</td>
</tr>
<tr>
<td rowspan="5">Atomic Coordinates</td>
<td rowspan="5">原子座標</td>
<td colspan="2">必要最小限の原子の座標が書いてある。</td>
</tr>
<tr>
<td>Atom, Form Factor</td>
<td>原子の種類</td>
</tr>
<tr>
<td>x, y, z</td>
<td>原子の座標(辺の長さに対する比)</td>
</tr>
<tr>
<td>PP</td>
<td>存在確率(VESTAではOcc.)</td>
</tr>
<tr>
<td>B</td>
<td>位置のゆらぎ(今回は使わない)</td>
</tr>
</tbody>
</table>

以上のデータをVESTAに入力していきます。

6. VESTAのメニューから[File]-[New Structure...]を選びます。  

<img class="alignnone size-full wp-image-3597" title="ze1" src="/img/ze1.png" alt="" width="490" height="446" /></a>

(再びこの入力画面を呼び出すには[Edit]-[Edit Data]-[Phase...]を選択します。)

7. [Title] (タイトル) に[物質名]を入力します。([New structure]と書いてあるところをクリックすると入力可能になる)
8. タブから[Unit cell] (単位格子) を選びます。

<img class="alignnone size-full wp-image-3598" title="ze2" src="/img/ze2.png" alt="" width="490" height="446" />

[Symmetry] (対称性) 中央のテーブル [Space group] から空間群の番号を選択します。  
(モルデナイトの場合、63)  
Crystal systemなどが自動で入力されます。  
[Setting]の指示がある場合、入力します。(それ以外の場合 1 のままでよい)  

> これらの項目を、原子座標を入力したあとに変更する際は、[Update structure parameters to keep 3D geometry]の項目を[Keep structure parameters unchanged]に変えてから入力する必要があります。

9. [Lattice parameters]に、単位格子の辺の長さと角度を入力します。  
(対称性によって定まる部分は、すでに入力されています。入力できない場合は、[Space group]の入力が間違っていると思われます。)  
s.u.の値はそのまま(0)でかまいません。

10. 原子座標の入力に入ります。
タブから[Structure parameters]を選びます。

<a href="/img/ze3.png"><img class="alignnone size-full wp-image-3599" title="ze3" src="/img/ze3.png" alt="" width="490" height="446" /></a>

[New]ボタンを押して、原子を追加します。  
[Symbol...]ボタンを押して、最初の原子の元素を指定します。  
[Label] には[Atom]に書いてある記号(例えばNA1)を入力します。  
[x], [y], [z]に、最初の原子の座標を入力します。  
[Occ.]に、[PP]の値を入力します。  
s.u.の値(0)、Bの値(1)はそのままでかまいません。

11. 原子の数だけ、10 を繰り返します。  
原子の数が多いときは、いくつかの原子を入力し終えたところで[OK]を押して、入力がうまくいっているかどうか確認した方が良いかもしれません。セーブも忘れずに。  
(水(H<sub>2</sub>O)については[Symbol...]をO(酸素)として入力するか、省略しても良いでしょう。)  
(原子の順序は、構造の表示には関係しません。)

12. 最後に[OK]を押します。


孔の空いた構造が正しく図示されたでしょうか。うまくいっていたら、忘れずにセーブしてください。

## 四面体ブロックの書き方
ゼオライトは SiO<sub>4  </sub>と AlO<sub>4  </sub>が構造の基本単位となっているので、この部分を四面体で描くと、構造がわかりやすくなります。

1. [Edit]-[Bonds...]を選択。[New]を押す。
2. [A1]に[Si]、[A2]に[O]を指定、[Max. Length]を2とする。
3. [Add]を押す。
4. アルミニウムが含まれている場合、同様に[A1]に[Al]、[A2]に[O]を指定、[Max. Length]を2として[Add]を押す。
5. [OK]を押す。
6. VESTAの画面の左側(最初の画面説明C)から表示スタイル [Polyhedral] (多面体) を選択。

## より広い範囲を描く
空間群による入力では、単位格子の繰り返しが簡単に行えます。

1. [Object]-[Bondary...]を選択。
2. [Ranges of fractional coordinates]が繰り返しの設定です。  
例えば、z(min) を -1 に、z(max) を 2 にしてください。
3. [OK]を押します。z 方向に単位格子が 3 回繰り返して描かれます。
   
入力途中は、こまめにセーブすることをお勧めします。

[前＜](advanced.md) [目次](/README.md) 
