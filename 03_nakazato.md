「遺伝子発現データベースを使い倒す」

        --
[[AJACSりんくう>AJACS14]] > 遺伝子発現データベースを使い倒す
        --

# はじめに [#y1166a60]
- みんなでわーっとアクセスすると、反応が遅くなったり、大量アタックと勘違いされてアクセス禁止（通称：アク禁）を食らったりするので、ばらばらとアクセスしてみてください
- というわけで、ここに書いてあること（や、他のところの）を自分なりに進めて or 自分なりにじっくりやってかまいません。
- 時間の都合で今日は省略させてもらうところがあります。ご承知おきください。
    -詳しく知りたい方は長めにやらせていただいた回の資料をご覧ください。
        -[[AJACS蝦夷2：「遺伝子発現データベースを使い倒す」>http://motdb.dbcls.jp/?AJACS12%2Fhono2]]
        -[[AJACS蝦夷2：「続・遺伝子発現データベースを使い倒す」>http://motdb.dbcls.jp/?AJACS12%2Fhono3]]


# （一応）自己紹介 [#dabf9afc]
- どんな人が、こういう（＝ライフサイエンス統合データベースセンターみたいな）ところにいるのか参考のために
- 99-02：wet時代（別名：バイオ時代）：東京工業大学（B4-M2）
    -恐山産ウグイの酸性適応機構
#fold(詳細,#ref(./wet.005.png))
    -ウナギの海水適応機構における硫酸イオントランスポーターの同定と機能解析
#fold(詳細,#ref(./wet.004.png))
- 02-07：dry時代（別名：IT時代）：NEC バイオIT事業推進センター
    -多くが製薬、食品に就職する中、実験に挫折。ITの道へ
    -文献検索システムの開発など
- 07：冬の時代：NEC（別部署）
    -部署が半壊（ビジネスにならなかった）。→ 別部署に飛ばされる
    -毎日、官庁相手の営業を支援するためのPowerPoint資料作り
- 07-：dry時代、再び
    -現在の職場に拾われる。

# 本題：遺伝子発現 [#c01f28b8]
## なぜ遺伝子発現なのか? （釈迦に説法） [#t3759669]
- そもそも分子生物学は、生命現象を分子レベルで解釈したい学問なわけで。
- ある生命現象（疾患、薬剤応答、...）で、どういう遺伝子の発現量が変化するかから、その生命現象のしくみをとらえる
- 個々の遺伝子が、いつ（ライフサイクルで、1日のうちで、など）、どこ（たとえば臓器レベル）で発現してはたらいているかを知ることにより、その生命現象のしくみをとらえる

## 発現データを用いて何ができるか [#lab3fa7c]
- 昔：個々の遺伝子の発現 → 今：全遺伝子の発現（マイクロアレイなど）
- ある生命現象の際に発現量の変動する（= その生命現象に関連の深い）遺伝子を抽出 → それらの関連から生命現象の仕組みを知る
    -簡単に言えば、ポンチ絵を描くなど

## [[&size(20){BioGPS};>https://biogps.gnf.org/]] &color(green){ヒト、マウス、ラットのさまざまな組織や細胞(株)における遺伝子発現プロファイルのデータベース}; [#yd1e24e9]

- 何コレ：さまざまな臓器、細胞株での個々の遺伝子の発現についてまとめたもの
- [[BioGPS>https://biogps.gnf.org/]]はAffymetrix社製のマイクロアレイであるGeneChipを用いた遺伝子発現プロファイルのデータベース。
- [[GNF SymAtlas>http://symatlas.gnf.org/]][[【参考動画】>http://togotv.dbcls.jp/20070816.html]]のメジャーアップデート版。
- マウスのエキソンアレイのデータが追加されたので、遺伝子のスプライシングバリアント(Splicing variant)の発現状況も調べることが可能。
- 検索した遺伝子に対して、種々の外部データベースに横断検索することができる。
### 【実習1】BioGPSを使ってある遺伝子の発現プロファイルを調べる [#j2eb939a]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20081004.html#p01]]、[[【講習会動画】>http://togotv.dbcls.jp/20090217.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[https://biogps.gnf.org/>https://biogps.gnf.org/]]を開きます。
- 2.水チャネル（水を通すトランスポーター）であるAQP3 (aquaporin 3) の発現プロファイルを調べてみましょう。中央の検索窓に「AQP3」と入力し、「search」を押します。
- 3. 表示された検索結果をクリックします。
- 4. 最初はヒトのマイクロアレイデータが表示されます。
- 5. マイクロアレイデータ左上の「Human」をクリックするとマウスやラットを選択できます。また、「203737_at」（プローブID）をクリックすると、別のプローブでの発現状況（別のsplice variantなど）の結果が見られます
- 6. AQP3はどの組織、細胞で強く発現しているでしょうか？
- 7. 右上の「default rayout」をクリックすると、検索した遺伝子に関するマイクロアレイデータ以外のデータが閲覧できますが、どのようなデータが閲覧できるのか調べてみましょう。
- 8. [応用] 左上の「Search」タグをクリックして検索画面にもどり、自分の興味ある遺伝子について同様に検索してみましょう。


## [[&size(20){NCBI Gene Expression Omnibus (GEO)};>http://www.ncbi.nlm.nih.gov/geo/]] [#gff484c3]
&color(green){世界最大の遺伝子発現（[[マイクロアレイ>http://ja.wikipedia.org/wiki/DNA%E3%83%9E%E3%82%A4%E3%82%AF%E3%83%AD%E3%82%A2%E3%83%AC%E3%82%A4]]）データベース（レポジトリ）};

塩基配列を研究者がGenBank (Nucleotide) に登録し、世界の人が見られるのと同じように、各々の発現情報も集められてみられるようになっています。それがGEOです。

- いろいろなデータ（DataSet, Sample, Platform）が出てきて混乱するかと思います。[[NCBI GEO Overview>http://www.ncbi.nlm.nih.gov/geo/info/overview.html]]が参考になるでしょう。

### 【実習2-1】GEOを使って、自分の興味のある遺伝子の（ある実験条件下における）発現状況を調べる [#l6c603ee]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20090213.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[http://www.ncbi.nlm.nih.gov/geo/>http://www.ncbi.nlm.nih.gov/geo/]]を開きます。
- 2.「Gene profiles」に自分の検索したい遺伝子名を入力します。
- 3. 今回は例として「[[nanog>http://www.google.co.jp/search?hl=ja&q=Nanog%E9%81%BA%E4%BC%9D%E5%AD%90]]」という遺伝子を検索してみましょう。入力終了後、「GO」をクリックします。
- 4. GEOに登録されている様々な実験条件で行なわれたマイクロアレイ実験における「nanog」遺伝子の発現データが表示されます。
- 5. 検索結果の右端にある画像をクリックすると、[[発現データの詳細をみる>http://www.ncbi.nlm.nih.gov/geo/gds/profileGraph.cgi?&dataset=DEAryz&dataset=yyyzzz$&gmin=5173.000000&gmax=11680.000000&absc=&gds=2294&idref=161072_at&annot=Nanog]]ことができます。
- 6. 「Display values」をクリックすると、発現値を一覧できます。
- 7. [[このサンプル>http://www.ncbi.nlm.nih.gov/sites/GDSbrowser?acc=GDS2294]]では、nanogはどういう細胞のどういう実験条件で発現が増減しているか調べてみましょう。
- 8. ページ下部の「samples」に列挙された[[リンク>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM130365]]をクリックすると、そのサンプル（一枚のマイクロアレイ）の詳細を閲覧できます。
- 9. [[リンク先のページ>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM130365]]の中ほどにある[[「series」のリンク>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE5583]]をクリックすると、この実験全体の詳細情報が見られます。
- 10. [[この実験全体の詳細情報ページ>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE5583]]の下部にある[[「Series Matrix File(s)」>ftp://ftp.ncbi.nih.gov/pub/geo/DATA/SeriesMatrix/GSE5583/]]をクリックすると、この実験の正規化補正済みのマイクロアレイデータをダウンロードすることができます。
### 【実習2-2】データセットブラウザ(Dataset browser)を利用して、GEOに登録されているマイクロアレイデータを解析する [#u5b85fd6]
- [[【使い方参考動画1】>http://togotv.dbcls.jp/20090221.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png 、[[【使い方参考動画2】>http://togotv.dbcls.jp/20090307.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[http://www.ncbi.nlm.nih.gov/geo/>http://www.ncbi.nlm.nih.gov/geo/]]を開きます。
- 2.「Gene profiles」に自分の検索したい遺伝子名を入力します。
- 3. 今回は例として「[[nanog>http://www.google.co.jp/search?hl=ja&q=Nanog%E9%81%BA%E4%BC%9D%E5%AD%90]]」という遺伝子を検索してみましょう。入力終了後、「GO」をクリックします。
- 4. GEOに登録されている様々な実験条件で行なわれたマイクロアレイ実験における「nanog」遺伝子の発現データが表示されます。
- 5. 検索結果の[[アクセッション番号（今回は GDS2294）>http://www.ncbi.nlm.nih.gov/sites/GDSbrowser?acc=GDS2294]]をクリックすると、解析用の「データセットブラウザ」が開きます。
- 6. 「Expression profiles」をクリックすると、[[この実験データセットにおける個々の遺伝子発現状況を検索できるページ>http://www.ncbi.nlm.nih.gov/sites/entrez?db=geo&cmd=search&term=GDS2294[ACCN]]に飛びます。
- 7. 検索窓に表示されているアクセッション番号の後に続けて遺伝子名を追加（今回は例として [[Oct4>http://www.google.co.jp/search?q=Oct4]] ）すると、この実験データセット内におけるその遺伝子の発現データが検索できます。
- 8. 「データセットブラウザ」の「Data Analysis Tools」では詳細なデータ解析が可能です。
- 9. 「Find gene name or symbol:」のところに自分の興味ある遺伝子名を入れてみましょう。
- 10. 「Find genes that are up/down for this condition(s):」の「GO」をクリックするとどのような遺伝子がヒットするでしょうか。
- 11. 「Compare 2 sets of samples」では2群間で発現に差のある遺伝子を（統計学的に）検索できます。step1で発現量の違いを検出する方法を設定します。step.2で比較する2群の設定をします。step.3の「Query Group A vs. B」をクリックすると、検索が始まります。
- 12. 「Cluster heatmaps」では、マイクロアレイデータ解析でよく用いられる[[ヒートマップ>http://images.google.co.jp/images?q=ヒートマップ]]でのデータ表示が行なえます。分類方法としてHierarchical、Partitional (K-means/K-medians)、By location on chromosomeの3種類が選べますが、それぞれどのようにデータが分類されるか試してみましょう。
- 13.  「Experiment design and value distribution」では実験データにおける発現の分布を参照できます。これにより、各サンプルのデータが互いに比較可能か（実験上のミスがないか）チェックすることができます。

### 【実習2-3】GEOを使って、自分の興味のあるマイクロアレイ実験データセットを検索&生データをダウンロードする [#m393c326]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20081218.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[http://www.ncbi.nlm.nih.gov/geo/>http://www.ncbi.nlm.nih.gov/geo/]]を開きます。
- 2. 画面中央の「Platforms」をクリックします。
- 3. [[Platform(マイクロアレイの種類)の一覧画面が現れる>http://www.informatics.jax.org/javawi2/servlet/WIFetch?page=imageSummaryByMrk&key=25000&imageType=8]]ので、上部の「FIND PLATFORM」をクリックします。
- 4. [[platformの検索画面>http://www.ncbi.nlm.nih.gov/geo/query/browse.cgi?mode=findplatform]]が現れるので、「Company name」に「Affymetrix」、「organism」に「Homo sapiens」を選択し、「FIND PLATFORM」をクリックします。
- 5. [[Affymetrixのヒトのマイクロアレイの検索結果>http://www.ncbi.nlm.nih.gov/geo/query/browse.cgi?mode=foundplatform]]が表示されるので、中程にある「Affymetrix GeneChip Human Genome U133 Plus 2.0 Array」の左端にある[[「GPL570」というID>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GPL570]]をクリックします。
- 6. [[表示された画面>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GPL570]]の真ん中あたりにある「series」下の「More...」をクリックすると、登録されているデータセットを閲覧できます。
- 7. ブラウザの検索ボタンなどを使って「reprogramming」という単語を検索するとどういうデータがヒットするでしょうか？
- 8. ヒットしたデータの左端にあるIDをクリックすると、[[そのデータセットの詳細情報>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE9832]]が閲覧できます
- 9. ページ下部の「Download family」の中にある「Series Matrix File(s)」をクリックすると正規化済みのデータのダウンロードリンクが表示されます。
- 10. ページ最下部の「Supplementary file」にあるリンクから生データをダウンロードすることができます。
- 11. 自分の研究テーマに近い、また興味のあるマイクロアレイデータが利用可能か検索してみましょう。

## 遺伝子発現バンク(GEO)目次：http://lifesciencedb.jp/geo/ [#r94c5b41]
- [[統合ホームページ>http://lifesciencedb.jp/]] > データベース > 遺伝子発現バンク(GEO)目次
- [ナニコレ] NCBIのGEO（Gene Expression Omnibus:mRNA発現情報のデータベース）に登録されている全レコードをプロジェクト単位で分類。「生物種」、「研究の型」、「部位」の三次元で分類。データを一括ダウンロード可能
- http://lifesciencedb.jp/image/small_video_icon.png [[遺伝子発現バンク(GEO)目次を使い倒す－その壱>http://togotv.dbcls.jp/20080623.html]]
- 【実習3-1】「生物種」で特定の種を選ぶと、研究プロジェクト数が絞り込まれることで数が変化する。「生物種」で「ヒト」を選ぶ前と後で「研究の型」の「GeneChip」(Affymetrixの発現アレイ)、「cDNAアレイ」、「オリゴアレイ」の項目はいくつからいくつに変化するか？また、「生物種」に「齧歯」を選ぶとそれぞれどうか？
- 【実習3-2】右上の検索フォームで'hypoxia'と入力して検索したあとで、「生物種」で「ヒト」、「研究の型」で「GeneChip」を選んで得られる研究プロジェクトのリストを表示せよ。「測定サンプル」のカラムの数字をクリックしてどのようなことが起こるか、確認してみよ。また、GSEで始まるGEOのエントリ（例えばGSE4725）をクリックするとNCBIのサイトに直接アクセスできるので、そのページにアクセスせよ。

### [[&size(20){DAVID: The Database for Annotation, Visualization and Integrated Discovery};>http://david.abcc.ncifcrf.gov/]] [#zef09660]
&color(green){マイクロアレイデータの生物学的な解釈};

#ref(./microarray.analysis.005.png)
- 上で述べたマイクロアレイの結果の解析は、統計解析で、それらの遺伝子が生物学的にどういう意味を持つかわかりません。
- そこで、Gene Ontologyの用語を付与することで、生物学的な解釈を行います。
- 【参考動画】[[DAVIDを使ってマイクロアレイデータを解析する>http://togotv.dbcls.jp/20090925.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
### 【実習4】DAVIDを用いて、発現データの結果を生物学的に解釈する [#y04a402a]
- 1. 上部メニューの「Start Analysis」をクリック
- 2. 画面左側バーで、probe IDリストをコピペ or ファイルを指定
    -今回は、統合TVと同じ、NCBI GEOより取得した公共の遺伝子発現データ（GSE1657:Adipocyte Differentiation [Homo sapiens]）を用いて、ヒトの脂肪細胞の分化過程で発現増加した[[上位500個の遺伝子群のリスト>http://motdb.dbcls.jp/?plugin=attach&refer=AJACS12%2Fhono3&openfile=090907_sample_U133A_adipo.txt]]を使って説明しています。
- 3. リストのIDの種類タイプを選択 … 今回は、「AFFY_ID」と「Gene List」
- 4. Submit List をクリック → 読み込まれる
- 5. 今、アップロードしたリストは、左側バーの「List Manager」で「Uploaded List_1」として保存されています。削除やrenameもできます。
- 6. 解析を続けます。真ん中の「Functional Annotation Tool」をクリック
- 7. 今回は、Gene Ontologyでの解析を行います。「Gene Ontology」をクリック → Gene Ontologyでの解析の細かいメニューが表示されます
- 8. 今回は、GOTERM_BP_ALL (BP=Biological Process)に注目します。その右の「Chart」をクリック → 結果がポップアップします
- 9. P-value を2回クリックしてp-valueが小さい（統計的に有意である）順にしてみましょう … p-value小さい順は、一度やればしばらく覚えているので、次からはしばらくは必要ないです
#fold(結果,#ref(./david.go_bp.png));
- [応用編] Pathways > KEGG_PATHWAY や Tissue Expression > UP_TISSUE なども見てみよう。生物学的にどういうことが言えるだろうか。



# 次世代シーケンサのデータについて [#w24271f5]
- 次世代シーケンサのデータは、中身は配列データですが、ある状態での遺伝子発現を塩基配列として検出することもでき、遺伝子発現データとしてもとらえられます
    -ゲノム解読として使う場合は、配列データとしてで、発現データを得るためにも用いることができる、ということです。
- 次世代シーケンサによる測定結果（≠解析結果）も、登録、公開のしくみができている
    -NCBI：Short Read Archive (SRA) http://www.ncbi.nlm.nih.gov/Traces/sra/sra.cgi
    -EBI：European Read Archive (ERA)
http://www.ebi.ac.uk/embl/Documentation/ENA-Reads.html
    -DDBJ：DDBJ Read Archive (DRA) http://trace.ddbj.nig.ac.jp/dra/index.shtml
- 【実習5】どのような形でデータが登録されているか見てみよう → [[例:http://tinyurl.com/lzlles]]
    -参考：[[DRA Documentation:http://trace.ddbj.nig.ac.jp/dra/documentation.shtml]]

        --
[[AJACSりんくう>AJACS14]] > 遺伝子発現データベースを使い倒す
        --
