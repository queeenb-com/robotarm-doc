# コロニーピッキングプロトコルの自動化の説明

## 1. コロニーピッキングの説明

コロニーピッキングは、微生物学や分子生物学の実験において、特定のコロニーを選択的に取り出すための手法です。このプロトコルは、特定の遺伝子や特性を持つ微生物を選別する際に非常に重要です。


## 2. 配布されているテンプレートの説明
コロニーピッキングを想定したテンプレートをご説明します。<br>
<img src="../images/nodedetails-samplenodes.png" alt="sample nodes" height="300"><br>
基本的には右に行くほど次のノードに進み、縦はループにおけるノードの実施順を表します。一番左のノードから説明をしていきます。


### 4.1 チップケースのデータフレームを作成する
最初のノードは「データフレーム作成」を用いたチップケースの穴の座標を集めた行列を作ります。
<div style="border-left: 4px solid #ffd700; background:rgb(230, 210, 172); padding: 15px; margin: 20px 0; border-radius: 5px;">
  <p style="margin: 0; font-size: 1.1em;">
    💡 <strong>Tips:</strong> <br>
   左右にある点は「in」「out」を表し、inにはその前に実行するノードをつなげ、outには次に実行するノードをつなげます。<br>
    <br>つまり基本的にはそれぞれのノードのin の点はoutにつながり、outの点はinにつながるということになります。
  </p>
</div>

### 4.2 シャーレの中のコロニーを認識する<br>
次のノードでは、コロニーを座標に変換して認識しています。コロニーの座標をループノードの中の「データフレーム移動」につなぐことでループのなかで一個ずつコロニーをピッキングしてもらいます。

### 4.3 レプリカ1を認識する<br>
次のノードでは、レプリカの座標を認識します。シャーレでレプリケーションをする際は、シャーレの中で四角ができるように座標をしてすることで方眼のようにレプリケーションを実施できます。



### 4.4 ウェルプレートを認識する<br>
次のノードでは、ウェルプレートの座標を認識します。行と列について間違えないようにしましょう。

### 4.5 ループを行うノードを作る<br>
次のノードでは、実際の自動化のプロトコルを作っていきます。

今回は「データフレーム移動」を四つつなげることで、ループを実現しています。移動する座標は「データフレームを渡す」という点を「データフレームを受け取る」という点につなげることで実現します。

チップケースに移動してチップをつける <br>
→ コロニーに移動してピッキング <br>
→ レプリカ1に移動してレプリケーション<br>
 → ウェルプレートに移動して落とす <br>
 
 が今回は行列の座標を受け取って実施しています。

その後、「指定座標移動」でチップを捨てるゴミ箱の上まで移動して、チップを排出しています。


### 4.5 ループが終わった後指定座標に移動させる<br>
ループが終わった後に実施したいノードは、ループノードの「ループ外へ」のノードと「in」をつなげることで実施できます。今回は、指定座標に移動してもらうために「指定座標移動」に好きな座標を入力して終了させています。

## 3. さらに拡張させるために
具体的に拡張させる方法について書き記していきたいと思います。

### 3.1 レプリケーションシャーレを増やしたい


## クイックナビゲーション

<div style="display: flex; flex-wrap: wrap; gap: 10px; margin-bottom: 20px;">
  <a href="/robotarm-doc/" style="display: block; padding: 10px 15px; background: #3498db; color: white; text-decoration: none; border-radius: 5px; min-width: 150px; text-align: center;">
    📖 メインガイド
  </a>
  <a href="/robotarm-doc/hardware.html" style="display: block; padding: 10px 15px; background: #e74c3c; color: white; text-decoration: none; border-radius: 5px; min-width: 150px; text-align: center;">
    🔧 ハードウェアマニュアル
  </a>
  <a href="/robotarm-doc/software.html" style="display: block; padding: 10px 15px; background: #f39c12; color: white; text-decoration: none; border-radius: 5px; min-width: 150px; text-align: center;">
    💻 ソフトウェアマニュアル
  </a>
  <a href="/robotarm-doc/nodesdetails.html" style="display: block; padding: 10px 15px; background: #2ecc71; color: white; text-decoration: none; border-radius: 5px; min-width: 150px; text-align: center;">
    🧩 ノード詳細ガイド
  </a>
  <a href="colonypicking.html" style="display: block; padding: 10px 15px; background: #9b59b6; color: white; text-decoration: none; border-radius: 5px; min-width: 150px; text-align: center;">
    🧪 コロニーピッキング
  </a>
</div>