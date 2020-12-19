# SS4E

# 20201219

課題：環上の加群、自由分解の理解、グレブナ―基底

# 20201218

http://www.kurims.kyoto-u.ac.jp/~kyodo/kokyuroku/contents/pdf/0786-02.pdf

http://www.kurims.kyoto-u.ac.jp/~kyodo/kokyuroku/contents/pdf/0802-08.pdf

http://www.kurims.kyoto-u.ac.jp/~kyodo/kokyuroku/contents/pdf/0820-18.pdf

http://www.pdmi.ras.ru/~lowdimma/BSD/Silverman-Arithmetic_of_EC.pdf

グレブナー基底１

グレブナー基底２

体とガロア理論

「先ず、線形符号とは群である」。この一言でこのテーマをやろうと決めた。

まず最初に具体例を作って生成行列から符号化を行い、復号関数を決めたい。

# 20201101

何だか漠然としたタイトルになってしまいましたが、鍵となるのは復号法を構成することだと言えそう。

例えばシンドロームエラー対応表を使ったとしても、復号できることには間違いない。
そのためには行が抜けた符号に対しても、エラーパターンとシンドロームの間に全単射的な写像が存在することが言えればいい。
そのための必要十分条件はなにか？

https://www.josephboutros.org/coding/RM_subcodes_2017.pdf


列を間引いても復号には問題がないけど、行を除くとどうにもならないのだろうか？
ユークリッドも、そのままでは使えなくなる。
SSRSにISDを使ったら復号できないのだろうか？
とにかくまだ何もない状態のようだが、全部調べたわけじゃないのでよくわからない。
これで3つの例を言ったことになる。

いろいろ探しているうちに、アフリカのセネガルの研究が目に止まった。

しかしざっと目を通してみると、暗号に使えるのではないかという予想を言っているだけで具体性がなかったので、
まだ誰も具体的には考えてないかもしれないという感じだった。
そもそも部分空間符号が定義できたからと言って、効率的な復号方法があるのかは議論されてない。

でも世界には自分と同じ考えを持つ人がいるということで、以外に狭いなとも思ってしまった。

# 20201024

幾何学的ゴッパ符号を調べるうちに、どんどん基礎にさかのぼって、もうこれ以上遡れないところにあったのがリードマラー符号だった。

で、これを使って組み合わせ論的に難しい暗号が作れそうだ、という感じで俄かにマイブーム。
平面上のすべての点を、２変数多項式で評価する、ということで面白そうな予感がしたのだ。
代数曲線の理論は難しいけど、有限幾何ならわかるかもしれない。
これで新型暗号は２つ目。
一個目はMcElieceの公開鍵に予めエラーを入れておくというもの。
これは別のリポジトリにある。
マスクと言われているものがこの方法だとすると既に後追い感のある研究だけど、こういうのは公開しているだけあって早い者勝ちだよなー。
でもここでは具体的に説明することはあえて避けて、code is the law,という感じで全部コード化して置いておく。

リードマラー符号は構造がとてもシンプルらしいので、幾何学的ゴッパ符号をやる前に、幾何学の基礎を符号に応用する練習になりそう。
多項式環上の加群とか、符号の自己同型の意味とかをこれでやるのがよさそうな感じ。
LDPC符号みたいに性能のいい符号の復号法も見つかるかもしれないし、いいことづくめだ。
だがここはあえて暗号に拘ってみる。

というわけで、グレブナ―も補間多項式もやる必要がなくなり、研究が一気に進展する可能性あり。

多数決論理復号とか置換復号とかが、この頃からあったという歴史の積み重ねを感じる。
もしかしたらリードマラーのほうが代数幾何符号なんて生煮えの理解しか得られない符号より、自分には合っているのかもしれないとか思う。
昔は、リードマラーなんか研究する価値のない古くて能力のない符号とか思ってて無視してたけど、名だたるものを追って、輝くものを追って、人は氷ばかりつかむ。

こういうネタは考えたからと言って思いつくものではなく、何かの拍子で無意識のうちに保存しておいた記憶が、ある瞬間に突然結びついて出てくるもののようだ。
人マネのほうが結果が分っているだけあって安心だけど、マネじゃないほうがいい。
マネじゃない事を祈る。

cf.
https://arxiv.org/pdf/2002.03317.pdf

https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.208.440&rep=rep1&type=pdf

https://www.researchgate.net/publication/334899262_Generalized_Subspace_Subcodes_With_Application_in_Cryptology/link/5d44a1ad92851cd0469c2161/download

https://cecas.clemson.edu/~keyj/Key/chapterAp.pdf

http://morpheo.inrialpes.fr/people/Boyer/Teaching/M2R/geoProj.pdf

https://www.researchgate.net/publication/281956646_Codes_and_finite_geometries

全然簡単じゃなかったｗ（早くも死にそう）

https://ia800700.us.archive.org/32/items/AlgebraicProjectiveGeometry/SempleKneebone-AlgebraicProjectiveGeometry.pdf

何だかよくわからん

http://www.math.boun.edu.tr/instructors/wdgillam/projgeo.pdf

初等幾何みたいにはならないよな・・・。

https://web.mat.upc.edu/simeon.michael.ball/IFG.pdf

これが一番イメージに近いかも

https://www.win.tue.nl/~ruudp/paper/29.pdf
