Pocket39
========

Pocket Miku
-----------

* ポケット・ミク [NSX-39](http://otonanokagaku.net/nsx39/)

なにこれ？
----------

ポケット・ミク ( [NSX-39](http://otonanokagaku.net/nsx39/) ) にひらがなで書いたテキストを読んで(歌って)もらうソフトです。

コンパイルには [dmc](http://www.digitalmars.com/d/download.html) が必要です。

開発は dmc 8.42n / Windows 8 で動作確認していますが、 Windows XP / Vista / 7 / 8.1 でも動くと思います。

(今は Windows 用のコードしかありませんが、将来別の環境でも作るかも。)

※ cmd.exe を UTF-8 が使える状態で起動してください。参照 ( [コマンドプロンプトでUTF-8を表示](http://nazochu.blogspot.jp/2011/08/blog-post_26.html) )

うたいかた
----------

    > pocket39
    きょうは、ぽけっとみくのつかいかたをせつめいします。
    ぽけみくは、おおえすのひょうじゅんにゅうりょくを、よみあげます。
    つまりこういうことです。
    ^Z
    > echo みくだよ | pocket39
    > pocket39
    おんていもつけられます。 / CEG[CEG[C]]GC]G[C
    うたうこともできます。
    ^Z
    > pocket39 < fuji3.p39

※こういうことはしないでください。

    > pocket39 < README.md

もくひょう
----------

- マニュアル作る
- パラメータの最大値最小値チェック
- 初期化時の MIDI Message (テンポ・ボリューム等)
- 開始前の無音期間指定
- RPN とか CC 送る？ (ミクの声は pitch bend sensitivity のデフォルト値が違う)
- ベロシティも各音または任意の位置で指定出来るようにしたい
- pitch bend の時の前の音との繋がりを考慮して envelope 出力する
- Sleep() でタイミングが適当なので FIFO 経由して timer thread で出力する予定
- note off は毎回ちゃんと送るべき？
- SMF ファイルの出力 あるいは .SMF <-> .p39 コンバータ造る
- .p39 ファイルにテンポ指定とかその他(発声以外の楽器指定とかコーラスとか)
- 声以外の楽器にも対応したい (ここまでするなら素直に MIDI コントローラで・・・)
- オフセット指定サポートで曲全体のキーを変えられるような・・・
- 歌詞と楽譜を一音ずつ混在する記述「あC240いE120うG60」をサポート予定
- 音の長さを「ー」の数で指定するとか
- あとで com サーバーにしてみる
- VST プラグインにも出来る？
- たぶんバグいっぱい

びこうらん
----------

- pocket39.py はテスト用です。参照 ( [OpenMIDI project](http://openmidiproject.sourceforge.jp/) )
- BSD license
