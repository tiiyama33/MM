# 単位格子を繰り返す (Q8のヒント)

「単位格子を繰り返す」という操作について、少し詳しく解説します。

鉄の単位格子(体心立方格子)を例として説明します。*x*, *y*, *z* の各方向に 3 回繰り返して、結晶構造を図示します。  
前の問題で、次のように単位格子を図示しました。  
<img class="alignnone size-full wp-image-3325" title="rep0" src="/img//rep0.png" alt="" width="160" height="160" />  
上の図には原子が 9 個書かれていますが、実際に 1 つの単位格子に含まれる原子数は 2 個なので、9 個の原子のうち 2 個を選び出します。  
<img class="alignnone size-full wp-image-3326" title="rep1" src="/img//rep1.png" alt="" width="160" height="160" /><a href="http://science.shinshu-u.ac.jp/~tiiyama/?page_id=3340">この時点のエクセルシート</a>  

>選ぶ原子 2 個はどれでもよいわけではありません。
>一番上の図に含まれる 9 個の原子のうち、各頂点にある 8 個の原子は、高校の時にそれぞれ 1/8 個と数えたことからもわかるように、「等価」です。この 8 個の中からひとつめの原子を選びます。  
>
><img class="alignnone size-full wp-image-3336" title="rep0-1" src="/img//rep0-1.png" alt="" width="160" height="160" />
>
>上の例では A を選びました。  
>他の頂点にある各原子－例えば B の位置にある鉄原子－は、次で行うように、隣の単位格子に含まれる原子(A のコピー)として表現されます。  
>中心にある C 原子だけは、周囲に単位格子を増やしても、表現できません。  
>よって、この中心にある原子をふたつめの原子として選びます。

次に単位格子に含まれる各原子を、*x* 軸方向に**単位格子の長さ分だけ平行移動した位置**の座標を追加します。

<img class="alignnone size-full wp-image-3337" title="rep2" src="/img/rep21.png" alt="" width="320" height="160" /><a title="問題 8 のヒント(2)" href="http://science.shinshu-u.ac.jp/~tiiyama/?page_id=11737">この時点のエクセルシート</a>  
これで単位格子 2 個分の結晶ができました。  
さらに 3 つめを作ります。  
<a href="/img/q8-nn3.png"><img class="alignnone size-full wp-image-3338" title="rep3" src="/img//rep3.png" alt="" width="320" height="160" />この時点のエクセルシート</a>  

3 × 3 × 3 = で 27 回、方向を変えつつこれを繰り返せば目的を達することができますが、少し楽をしましょう。  
ここまでに作った単位格子 3 個分、6 個の鉄原子**すべて**をコピーし、 *y* 軸方向に単位格子の長さ分だけ平行移動させます。  
<a href="http://science.shinshu-u.ac.jp/~tiiyama/?page_id=11743"><img class="alignnone size-full wp-image-3352" title="rep6" src="/img//rep6.png" alt="" width="320" height="220" />この時点のエクセルシート</a>  
これで単位格子 6 個分が終了しました。  
先ほどの 6 個の原子を使って、もう 1 列作ります。  
<img class="alignnone size-full wp-image-3350" title="rep9" src="/img/rep9.png" alt="" width="320" height="220" /><a href="/img/q8-nn5.png">この時点のエクセルシート</a>  

あとは大体想像がつくと思いますが、ここまでで作った単位格子 9 個分、鉄原子 18 個**すべて**を *z* 軸方向にずらして 2 回コピーすれば、目的の構造が完成します。  
<img class="alignnone size-full wp-image-3348" title="rep27" src="/img//rep27.png" alt="" width="420" height="360" /><a href="/img/q8-nn6.png">この時点のエクセルシート(の一部)</a>  
原子半径を使って描いてみましょう。  

|<img class="size-full wp-image-3354" title="rep27-Fe" src="/img/rep27-Fe.png" alt="" width="420" height="360" />|
|:---:|
|鉄原子をSpace-fillingで書いた結晶構造|

実際の結晶は、単位格子を各方向に数十回から数千回以上繰り返した構造を持っています。  

コンピュータの利点は反復計算に強いことなので、このように情報をうまく整理することで、効率よく目的の演算を行うことができます。  
