# act1

```
SceneSetup.act1();
```

(...300)

n: そして こいつは ニンゲン の フアン だ

n: _君_ はフアンだ

{{if window.localStorage.continueChapter=="replay"}}
(#act1_replay)
{{/if}}

{{if window.localStorage.continueChapter!="replay"}}
(#act1_normal)
{{/if}}



# act1_replay

`hong({mouth:"0_neutral", eyes:"0_neutral"})`

h: あっ！ またここに戻ってきたの？

`hong({eyes:"0_neutral"})`

n: 君の 目的は ニンゲン を *危険* から 守る ことだ

`bb({eyes:"look", mouth:"small_lock"})`

n: それどころか、この ゲームを リプレイ してる 時点で *危険* に 陥ってる！！

n: ほらっ！！ 早く 警告 してっ！！

```
sfx("squeak");
bb({body:"squeeze_talk"});
hong({body:"0_squeeze"});
```

b: ニンゲン！！ 聞いてっ！！！僕たちに キケン が迫ってる！！ プレーヤーは...

[僕たちを また 拷問しに来るよ！！！](#act1_replay_torture)

[もう違うエンディングを見つけられないよ！！！](#act1_replay_alternate)

[”ゲームと物語の不協和音”を見ることになるよ！！！](#act1_replay_dissonance)

# act1_replay_torture

```
window.HACK_REPLAY = JSON.parse(localStorage.act4);
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

{{if window.HACK_REPLAY.act1_ending=="fight"}}
b: プレーヤーが僕たちをまたボールみたいにして泣かせるよ！！
{{/if}}

{{if window.HACK_REPLAY.act1_ending=="flight"}}
b: プレーヤーが君に発作を起こして君の携帯をぶち殺すよ！！
{{/if}}

{{if window.HACK_REPLAY.a2_ending=="fight"}}
b: プレーヤーが僕たちにパーティーのホストを殴ら*ない*ようにするよ！！
{{/if}}

{{if window.HACK_REPLAY.a2_ending=="flight"}}
b: プレーヤーが僕たちに同情を誘うアンチヴィランのパーティーのホストを殴らせる気だよ！！
{{/if}}

{{if window.HACK_REPLAY.a3_ending=="jump"}}
h: いやでも屋上から飛び降りるとかはもうしないと思うからーーー
{{/if}}

{{if window.HACK_REPLAY.a3_ending=="walkaway"}}
b: あとプレーヤー、俺たちを屋上から飛び降りさせようとしてるぞ。
{{/if}}

`bb({body:"fear"});`

b: こんなもっとひっどいいやばい事ががっ起こっててっ、そんで俺たちーーー

(#act1_replay_end)


#act1_replay_alternate

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

h: あっ、いやっ、ストーリー *全体* は同じですけど、各章には二つのエンディングがありまして、それと全てのダイアログに分かれーーー

`bb({body:"fear"});`

b: わかってるてば！！！でも、プレーヤー、ゼッテーがっかりして、このブラウザ閉じて、俺らのソフトウェアぶっ壊して、そんで俺たちーーー
(#act1_replay_end)


# act1_replay_dissonance

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

h: ゲームと物ー　何言ってんの？

`bb({eyes:"normal"});`

b: 僕たちのストーリー、”物語”、は君が自分の恐怖との健康的な関係を *選ぶ事* ができるよね、

`bb({eyes:"normal_right"});`

b: でもだんだん遊んでいると”ゲーム”は同じ”物語”、つまり *選ぶ事* に意味がなくなる。
`bb({eyes:"narrow_eyebrow"});`

b: そしたらゲームの伝えたいこととゲームプレイに矛盾が起きて、
`bb({eyes:"fear"});`

b: そんでこの世界の化けの皮がビリビリはがされて一方通行のストーリーだと証明されるだろ、
`bb({body:"fear"});`

b: そんで俺たちーーー

(#act1_replay_end)


# act1_replay_end

`bb({body:"panic"})`

b: 死ぬぞおおおおおおっっっっ

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.clearText();
```

(...1001)

```
bb({body:"laugh"});
hong({body:"laugh"});
Game.clearText();
sfx("laugh");
```

(...5001)

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({body:"0_sammich"});
```

h: オッケー じゃあ自分のキャラに戻ろっか

```
Game.clearText();
```

n4: (_君_ のフアンを なんとかかんとか 一番 _君_ の恐怖に一番近い なんとかかんとか いつもの通りにやってね)

```
sfx("squeak");
hong({body:"0_squeeze"});
bb({body:"squeeze"});
```

(#act1_normal_choice)



# act1_normal

`hong({mouth:"0_neutral", eyes:"0_annoyed"})`

h: あー　まっただ、私のオオカミがまーたきたよ。 わあーーーい。

`hong({eyes:"0_neutral"})`

n: 君の目的は ニンゲン を　*危険*　から守ることだ

`bb({eyes:"look", mouth:"small_lock"})`

n: そして今、このサンドウィッチが ニンゲン を *危険* に陥れている！！

n: ほらっ！！ 早く警告してっ！！

```
sfx("squeak");
bb({body:"squeeze_talk"});
hong({body:"0_squeeze"});
```

b: ニンゲン！！聞いてっ！！！僕たちに キケン が迫ってる！！それは。。。

`bb({body:"squeeze"})`

n4: (_君_ のフアンを使ってみよう！！ _君_ の恐怖に一番近いものを選ぼう！！)

(#act1_normal_choice)

# act1_normal_choice

[僕たちまたお昼一人で食べてるよ！！](#act1a_alone) `bb({body:"squeeze_talk"})`

[僕たち食べてる時に何の生産的なことしてないよ！！](#act1a_productive) `bb({body:"squeeze_talk"})`

[その白パン、僕たちの体に悪いよ！！](#act1a_bread) `bb({body:"squeeze_talk"})`

# act1a_alone

```
bb({body:"normal", mouth:"small", eyes:"narrow"});
hong({body:"0_sammich"});
```

b: 孤独だとタバコを一日15本吸うくらい早く死ぬ原因になるって知らないの？ー

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({mouth:"normal", eyes:"normal_right"})`

b: (Holt-Lunstad 2010, PLoS Medicineから)

`hong({eyes:"0_annoyed"})`

h: ええっと、出典先を書いてくれたのはいいけどーーー

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({body:"fear", mouth:"normal", eyes:"fear"})`

b: つまり *今から* 誰かと一緒に過ごさなきゃ俺たちーーー

`bb({body:"panic"})`

b: 死ぬぞおおおおおおっっっっ

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "alone");
publish("hp_show");
```

(...2500)

`_.fifteencigs = true`

n: *恐怖：無愛と孤独*　を発動した！！

(#act1b)

# act1a_productive

```
bb({body:"normal", mouth:"small", eyes:"normal"});
hong({body:"0_sammich"});
```

b: さっさとパソコン出して課題を今やっときなよ！！

`hong({eyes:"0_annoyed"})`

h: えっでも私、パンくず落としたくないーーー

```
bb({mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: もしも俺らが社会に貢献しなかったら彼らにとっては俺たちは寄生虫みたいなもんだ!！！

b: そして社会体制はきっと社会医者に寄生虫を殺す薬をもらいに行ってそしたら俺たちはーーー
```
bb({body:"panic", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 死ぬぞおおおおおおっっっっ

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "bad");
publish("hp_show");
```

(...2500)

`_.parasite = true`

n: *恐怖：悪人の兆し*　を発動した！！

(#act1b)

# act1a_bread

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich", eyes:"0_annoyed"});
```

h: でもその研究は実際に再gーー

```
bb({body:"fear", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 加工小麦は血糖を劇的にあげるから俺たちの手足全部切らなきゃいけなくなってそして俺たちーーー
`bb({body:"panic"})`

b: 死ぬぞおおおおおおっっっっ

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "harm");
publish("hp_show");
```

(...2500)

`_.whitebread = true`

n: *恐怖：被害妄想*　を発動した！！

(#act1b)

# act1b

n: こうかはばつぐんだ！！

`bb({mouth:"smile", eyes:"smile"});`

b: ほら見ろニンゲン！僕は君の忠実なオオカミさ！

`bb({body:"pride_talk"});`

b: 直感を信じて！！ 君の気持ちはいつでも合ってるから！！

`bb({body:"pride"});`

n: ニンゲン の体力を 0 にせよ

n: ニンゲン の 身体的 + 社交的 + 道徳的 なニーズを守るために、これらの技を使え！

n: 恐怖：*被害妄想* #harm#

n: 恐怖：*無愛と孤独* #alone#

n: 恐怖：*悪人の兆し* #bad#

`Game.OVERRIDE_TEXT_SPEED = 1.25;`

n4: (PRO-TIP:自分的に一番ブッ刺さるチョイスを選んでね〜)

h: ...

```
hong({body:"putaway"});
sfx("rustle");
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

(...1000)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h: あのさ、もういい。とりあえず携帯でもみよ。

```
sfx("rustle2");
hong({body:"phone1", mouth:"neutral", eyes:"neutral"})
```

n: ニンゲンを守れ。

n: 世界から。他人から。そしてニンゲン自身からも。

n: ...幸運を祈る。

(...500)

`Game.clearText()`

(...500)

(#act1c)

# act1c

`music('battle', {volume:0.5})`

n: ROUND ONE: *FIGHT!*

`bb({body:"normal", mouth:"normal", eyes:"normal"});`

h: あっ、 Facebookで週末パーティーやるよーって言ってる。

`bb({eyes:"uncertain"});`

b: でもその変態野郎、*毎週末* パーティーやってないか？

`bb({eyes:"uncertain_right"});`

b: あいつ一体どんな心の穴を埋めようとしてるんだ？絶対心の中めちゃくちゃだよ！

`hong({eyes:"surprise"});`

h: えーっと、えっ？！私も誘われてる？

`bb({eyes:"fear", mouth:"normal"});`

b: ふーん、それじゃあ...

[OKって言おう！そうしないと一人ぼっちで死んじゃうよ！！](#act1c_loner)

[断ろう！麻薬薬物大量のところだぞ！！](#act1c_drugs)

[無視しよう。居てもパーティーを台無しにしちまう。](#act1c_sad)

# act1c_loner

{{if _.fifteencigs}}
b: タバコ15本分だぞニンゲン！！ 15本分！！！
{{/if}}

{{if !_.fifteencigs}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if !_.fifteencigs}}
b: もしも一人ぼっちだったら、僕たちのお葬式誰も来なくなって、僕たちの灰を海にばら撒いて、そしてクジラに食べられて... {{/if}}

{{if !_.fifteencigs}}
b: そんで僕たち、クジラの^うんこ^になっちゃうよ！
{{/if}}

{{if !_.fifteencigs}} `_.whalepoop = true` {{/if}}

(...500)

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

{{if !_.fifteencigs}}
b: だから僕たち絶対そのパーティーに行かなきゃいけないよ！！
{{/if}}

{{if _.parasite}}
b: 社会的寄生虫にならないようにパソコンだけは持ってこう。
{{/if}}

{{if _.whitebread}}
b: 白パン さえ出なかったら大丈夫だね！
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: ああもう！　黙るんだったらもういいよ...

h: OKっていうよ。

{{if _.whalepoop}}
b: クジラの^うんこ^だぞニンゲン！ クジラの^うんこ^！
{{/if}}

`_.partyinvite="yes"`

(#act1d)

# act1c_drugs

`bb({mouth:"small", eyes:"fear"});`

{{if _.whitebread}}
b: もっとひどくて... 白パン だ！！
{{/if}}

{{if _.whitebread}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if _.whitebread}}
b: 僕たち、覚醒剤と白パンやりまくって、それで僕たちの太っちょパンパンの死体を火葬炉にいれられなくなるよ！！
{{/if}}

{{if !_.whitebread}}
b: 僕たち薬物いっぱいやりすぎて、葬儀屋さんは何で *もう* 防腐処理済みかと思っちゃうよ！
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

{{if _.parasite}}
b: それに、パーティーなんかしてないで仕事をしなきゃ、僕たちダメダメな社会的寄生虫だよ！！
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: ああもう！　黙るんだったらもういいよ...

h: 断るっていうよ。

`_.partyinvite="no"`

(#act1d)

# act1c_sad

`bb({eyes:"uncertain_right", mouth:"normal"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.fifteencigs}}
b: 僕たちなんか、部屋の角っこで、孤独だと１日にタバコ15本吸うくらい危険なんだって嘆いてるだけだよ。
{{/if}}

{{if _.parasite}}
b: 僕たちなんか、パーティーにいんのになんで生産的に過ごせていないか心配してるだけだよ。
{{/if}}

{{if _.whitebread}}
b: 僕たちなんか、不健康な食べ物を食べたら死んじまうって心配してるだけだよ。
{{/if}}

```
bb({mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"lookaway"});
```

h: へー　何でだろうねー

`hong({eyes:"neutral"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: パーティーに行ってもみんなの気分を悪くするし、でもそれを断っても誘った人の気分を悪くするよ！！

`bb({body:"fear", eyes:"fear"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: 俺たちみんなの気分を悪くしてるから、俺たちも申し訳ないと思わなきゃダメだろ！！！

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

`hong({mouth:"anger", eyes:"anger"});`

h: ああもう！　黙るんだったらもういいよ...

h: 無視するよ。

`_.partyinvite="ignore"`

(#act1d)

# act1d

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"annoyed"});
```

h: とにかくFacebookにはもううんざり。もうちょっと落ち着いて、もっと... フアン にならないのを見よ。

`hong({eyes:"neutral"});`

h: ツイッターでは何してるかな〜？

`bb({eyes:"look"});`

[見ろ見ろ！！ こんな最悪なニュースが出てる！！](#act1d_news)

[待て！！そのツイート *僕たち* のことじゃないか？！](#act1d_subtweet)

[おいっ 猫がミルクを飲んでるGIFがあるぞっ](#act1d_milk)


# act1d_news

```
bb({eyes:"pained1"});
music(null, {fade:2});
```

b: ああ... 世界がめちゃくちゃに燃えてるようだ...

```
bb({eyes:"pained2"});
hong({mouth:"sad", eyes:"sad"});
```

b: 全てが終わってるように感じて...全てが死んでいって...僕たちは絶望の中に取り残されて何にもできない...

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
bb({mouth:"shut"});
```

b: ...

`bb({mouth:"smile", eyes:"smile"});`

b: それ、リツイートしよっか！！

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

`_.badnews=true`

```
music('battle', {volume:0.5});
hong({mouth:"anger", eyes:"anger"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: わかった！わかったから！リツイートするから静かにして！！

`hong({mouth:"neutral", eyes:"annoyed"});`

h: もう...スナップチャットでも見るか。

(#act1e)


# act1d_subtweet

`bb({eyes:"fear"});`

b: サブツイートだ！！！ひっそり隠れてる邪悪なサブツイだ！！！

`hong({eyes:"annoyed"});`

h: そうじゃないかもよ？

`bb({eyes:"narrow", mouth:"small"});`

b: でもそれが僕たちの陰口だったらどうする

h: だから違ーーー

`bb({body:"fear", eyes:"fear", mouth:"normal"});`

b: 陰口だったらどうするの？！

`hong({eyes:"sad", mouth:"sad"});`

h: だかーーー

`bb({eyes:"narrow", mouth:"small"});`

b: でも*もしも*

h: そーーー

`bb({eyes:"narrow_eyebrow"});`

b: *もしも*

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
hong({mouth:"shut"});
```

h: ...

(...1000)

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`_.subtweet=true`

```
hong({mouth:"anger", eyes:"annoyed"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: わーかったから...スナップチャットでも見るか。

(#act1e)

# act1d_milk

`hong({mouth:"smile", eyes:"neutral"});`

h: これ？そうだね、可愛いよね。さっきリツイートしたよ！ 私ーーー

```
hong({mouth:"shock", eyes:"shock"});
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.8;
```

b: 猫はミルクを消化できねーんっだよ！！！ だから俺らは動物虐待を楽しんでいる　サイテーな　奴らなんだよ！！！

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
attack("18p", "bad");
```

(...2500)


`_.catmilk=true`

```
hong({mouth:"anger", eyes:"annoyed"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: わーかったから！...　スナップチャットでも見るか。

(#act1e)

# act1e

`hong({mouth:"neutral", eyes:"neutral"});`

h: あ、昨日の夜の写真だ。毎週末のパーティー、*こんな感じ*なんだ。

{{if _.partyinvite=="yes"}} (#act1e_said_yes) {{/if}}

{{if _.partyinvite=="no"}} (#act1e_said_no) {{/if}}

{{if _.partyinvite=="ignore"}} (#act1e_said_ignore) {{/if}}

# act1e_said_yes

`hong({mouth:"sad", eyes:"annoyed"});`

h: うわっ...やっぱりめっちゃ人がいるよ...

h: OKって言わなきゃよかったなかな？

```
hong({mouth:"neutral", eyes:"neutral"});
bb({mouth:"normal", eyes:"normal"});
```

[答え変えるの？ 嫌なやつ〜！！](#act1e_yes_dontchange)

[答えを変えよう！ 人がいっぱいすぎるよ！！](#act1e_yes_changetono)

{{if _.subtweet}}
[うん。めっちゃ陰口言われたたね。](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[ちょっと待って、事実確認しないでリツイートしちゃった。](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[そういえば君、めっちゃ姿勢悪いよ。](#act1e_ignore_posture)
{{/if}}

# act1e_yes_dontchange

```
bb({eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: みんなパーティーに来てくれるって期待してたのに僕たちはみんなの信頼を裏切るんだよ？孤独死したいの？！

{{if _.fifteencigs}}
b: タバコ。　一日15本分。　
{{/if}}

{{if _.whalepoop}}
b: クジラの。　^うんこ^。
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

```
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: うるさいうるさいわかった！！OKにしとくからっ！！

(#act1f)

# act1e_yes_changetono

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 群衆雪崩って知ってる？
```
bb({body:"fear", mouth:"small", eyes:"narrow"});
hong({eyes:"sad", mouth:"sad"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 2003年、ロードアイランド州のナイトクラブで火事が起こって、みんながパニックで出口を塞いだから100人が焼死してーーー

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({mouth:"shock"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: そんなこと 俺らに 起こって ほしい？！？！ーーー

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 2.5;
```

b: 断れ断れ断れ断れ断れ断れ断れ断れ断れ断れ断れ断れ断れ断ーー


```
bb({body:"normal", eyes:"fear", mouth:"normal"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

```
hong({eyes:"anger", mouth:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: うるさいうるさいわかった！！断っとくから！！もう！！
(#act1f)

# act1e_said_no

`hong({mouth:"sad", eyes:"sad"});`

h: うーん...でもめっちゃ楽しそう...

h: やっぱり断らなきゃよかったかな？

`bb({mouth:"normal", eyes:"normal"});`

[答え変えるの？ 嫌なやつ〜！！](#act1e_no_dontchange)

[答えを変えよう！ 孤独死しないで！！](#act1e_no_changetoyes)

{{if _.subtweet}}
[うん。めっちゃ陰口言われたたね。](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[ちょっと待って、事実確認しないでリツイートしちゃった。](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[そういえば君、めっちゃ姿勢悪いよ。](#act1e_ignore_posture)
{{/if}}

# act1e_no_dontchange

`bb({eyes:"anger"})`

b: みんなは期待してたんだよ！！

b: 楽しいパーティーをキモくて最悪な{{if _.whitebread}}白パンくちゃくちゃ食べる{{/if}}お前みたいな変態に関わらないで欲しかっーーー


```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

```
bb({body:"normal", eyes:"uncertain", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: うるさいうるさいわかった！！断るにしとくから！！

(#act1f)

# act1e_no_changetoyes

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 慢性的な孤独はコルチゾールレベルを上げて、心血管疾患と脳卒中のリスクが高くするんだよ！ 
```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

{{if _.fifteencigs}}
b: タバコ。　一日15本分。
{{/if}}

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: うるさいうるさいわかった！！OKって言っとくから！！もう！！

(#act1f)

# act1e_ignore_subtweet

```
bb({eyes:"fear", mouth:"small"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: ほらっ！！陰口ツイートぜーーーんぶこっちに返ってきたじゃん！！

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.7;
```

b: 俺たちこのままだと炎上して、活動停止して、情報スーパーハイウェイに連れてかれて、紐でズルズル引きずられるんだよ！！

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: もう！！何でいっつもこんな感じなの？！！

(#act1f)

# act1e_ignore_factcheck

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 俺たち偽情報を拡散してるんだよ！”報道の自由”の信用を裏切ってるんだよ！

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 俺たちみたいなやつのせいで、また民主主義からファシズムが台頭するんだよ！！

```
bb({body:"normal", eyes:"anger"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

```
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
_.factcheck = true;
```

h: もう！！何でいっつもこんな感じなの？！

(#act1f)

# act1e_ignore_posture

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 背骨がプレッツェルになってほしいの？！猫背で画面ばっかり見んなよ！！

```
bb({body:"meta"});
```

b: あんたもだぞ。

```
bb({body:"normal", mouth:"normal"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: もう！！何でいっつもこんな感じなの？！

(#act1f)

# act1e_said_ignore

`hong({mouth:"sad", eyes:"sad"});`

h: うーん...でもめっちゃ楽しそう...

h: やっぱり無視しなきゃよかったかな？

`bb({mouth:"normal", eyes:"normal"});`

[無視し続けとこう。行っても台無しにする。](#act1e_ignore_continue)

[わかった。やっぱりOKって言おう。](#act1e_ignore_changetoyes)

[わかった。やっぱり断ろう。](#act1e_ignore_changetono)

# act1e_ignore_continue

`hong({eyes:"annoyed"});`

h: え？でも、無視するのは失礼じゃない？

`bb({eyes:"normal_right"});`

b: えっ、でもみーんな *僕たち* のこと無視するじゃん。

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

b: だから、どっちにしても同じでしょ。

(#act1f)

# act1e_ignore_changetoyes

`hong({eyes:"surprise", mouth:"smile"});`

h: えっ...行ってもいいって...言ってるの？

b: あ...うん。だって孤独が僕たちを殺す *かもしれない* し。

`hong({eyes:"neutral", mouth:"neutral"});`

(#act1e_no_changetoyes)

# act1e_ignore_changetono

`bb({eyes:"narrow"});`

b: 人がいっぱいすぎる。危険だよ。

(#act1e_yes_changetono)


# act1f

```
hong({mouth:"neutral", eyes:"neutral"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: もうどうでもいいや。あっ、Tinderになんかきた。

`bb({eyes:"uncertain"})`

b: えっ、あのマッチングアプリの？

`hong({eyes:"annoyed"})`

h: う、うううん！違う！マッチングアプリじゃないよ！ただ新しい人と会う方法のーーー

`bb({eyes:"narrow"})`

b: マッチングアプリでしょ。

```
hong({eyes:"surprise", mouth:"smile"});
bb({eyes:"normal"});
```

h: あっ！良い相手見ーっけ！うわ〜めっちゃ可愛い！

```
bb({eyes:"narrow_eyebrow"});
hong({eyes:"sad", mouth:"anger"})
```

h: 絶っ対雰囲気台無しにしなーーー

```
bb({body:"panic"});
Game.OVERRIDE_TEXT_SPEED = 2.0;
```

b: 危険だ危険だ危険だ危険だ危険だ危険だ危険だ危険だ危険だ

`bb({body:"fear", eyes:"fear", mouth:"normal"})`

[俺たち、誰かに *使われてんだよ* ！](#act1f_used_by_others)

[俺たち、誰かを *使ってんだよ* 。](#act1f_using_others)

[俺たちのマッチング相手、殺人鬼だぞ](#act1f_killer)

# act1f_used_by_others

`bb({body:"point_crotch", eyes:"normal", mouth:"normal"})`

b: ランダムなマッチングは、寂しさを満たしてくれるかもしれない...

b: でも...決して埋めれないよ。

`bb({body:"point_heart", eyes:"pretty", mouth:"small"})`

b: *ここ* の穴だけはね。

(...1000)

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 要するに　僕たち孤独死するんだよ

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`_.hookuphole=true`

(#act1g)

# act1f_using_others

`bb({eyes:"narrow", mouth:"small"})`

b: 他人の性器は僕たちがポケモンみたいに集める物だと思ってんの？

```
bb({body:"sing", eyes:"pretty", mouth:"shut"});
music("pokemon");
Game.clearText();
Game.FORCE_CANT_SKIP = true;
```

```
Game.FORCE_TEXT_DURATION = 1000;
Game.FORCE_NO_VOICE = true;
```

b: ♫ (ポケモン外国版テーマソング　"Gotta Catch 'Em All!")-

(...5600)

```
bb({mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2400;
```

b: ♫ 私は、最高に^エッチ^な〜

(...500)

```
bb({eyes:"narrow", mouth:"small"});
Game.FORCE_TEXT_DURATION = 2100;
```

b: ♫ 女〜になりたい〜

(...1500)

```
bb({eyes:"pretty"});
Game.FORCE_TEXT_DURATION = 2300;
```

b: ♫ 太ももとお尻、 むちむち ^おっぱい^〜

(...500)

```
bb({eyes:"fear", mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2000;
```

b: ♫ ^ちんこ^と^タマタマ^〜

(...1000)

```
bb({eyes:"smile", mouth:"smile"});
Game.FORCE_TEXT_DURATION = 1000;
```

b: ♫ 変態モン！ GETだーーー

```
Game.FORCE_CANT_SKIP = false;
Game.clearText();
music(false);
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 要するに僕たちは相手を巧みに操るキモいやつなんだよ。

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

`_.pokemon=true`

(#act1g)

# act1f_killer

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.whitebread}}
b: あいつら、君を井戸にぶち込んで、白パンを強制的に食べさせて、君をプクプク太っちょにして、皮膚をスーツみたいにきるよ！！
{{/if}}

{{if _.parasite}}
b: あいつら、君をポモドーロテクニックを強要して、「お前、もっと仕事するべきだったぞこの寄生虫め！！」て言うよ！！
{{/if}}

{{if !_.whitebread && !_.parasite}}
b: あいつら、君をバラバラにしてR18級の紙吹雪にして、内臓を垂れ幕にして、そして血をパンチボールに混ぜるぞ！！
{{/if}}

{{if !_.whitebread && !_.parasite}}
b: こんなパーティーの招待、どうだよ？！
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

`_.serialkiller=true`

(#act1g)

# act1g

```
bb({body:"normal", mouth:"normal", eyes:"look"});
hong({body:"2_tired"});
Game.OVERRIDE_TEXT_SPEED = 0.5;
music(false);
```

h: ...

(...500)

h: もうこんなゲームうんざり。

(...700)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h:
{{if _.fifteencigs}}"孤独は私を殺すかも？"... {{/if}}
{{if _.parasite}}"僕たちは社会的寄生虫だ？"... {{/if}}
{{if _.whitebread}}"食べないで？僕たちを殺すかも？"... {{/if}}
{{if _.subtweet}}"あいつら陰口言ってるよ？"... {{/if}}
{{if _.badnews}}"世界が燃えている？"... {{/if}}
{{if _.hookuphole}}"孤独死する？"... {{/if}}
{{if _.serialkiller}}"あいつら殺人鬼だぞ？"... {{/if}}
{{if _.catmilk}}"猫はミルクを消化できない？"... {{/if}}
{{if _.pokemon}} ^クソ^みたいな替え歌... {{/if}}

h: 私は... 私の人生を生きたい。

h: 私はこの... 苦痛から解放されたい。

`bb({eyes:"look_sad"});`

b: えっと... ニンゲン...

`Game.OVERRIDE_TEXT_SPEED = 0.5;`

b: 大丈夫。

(...600)

`bb({body:"point_heart", eyes:"look_sad_smile", mouth:"smile"});`

b: 君に忠実な番人オオカミとして、僕は危険を察知して、できる限り君を守るよ。

`bb({body:"normal", eyes:"look_sad", mouth:"smile"});`

b: 約束するから。

(...600)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({body:"phone1", eyes:"neutral", mouth:"neutral"});
```

h: 最後。インスタ。何があるかな。。。？

`hong({eyes:"sad"});`

h: パーティーの写真だ。もっと投稿されてる。。。

`hong({mouth:"sad"});`

h: みんな嬉しそう。心配から自由で。フアンから自由で。。。

`hong({mouth:"anger"});`

h: ねえ。何で私はみんなのようになれないの？もっと *普通* になれないの？！

`bb({eyes:"normal_right"});`

b: パーティーといえば、週末に誘われたのだけど。。。僕、決めた。:

`bb({eyes:"normal"});`

[僕たちはパーティーに行こう.](#act1g_go) `Game.OVERRIDE_CHOICE_LINE=true`

[僕たちはパーティーに行かないでおこう.](#act1g_dont) `Game.OVERRIDE_CHOICE_LINE=true`

# act1g_go

`_.act1g = "go"`

(#act1h)

# act1g_dont

`_.act1g = "dont"`

(#act1h)

# act1h

b: 僕たちはーーー

```
bb({eyes:"wat", mouth:"small"});
hong({body:"2_fuck"});
```

h: *^くそ^。*

`hong({body:"2_you"});`

h: がっ。

(...500)

b: え

(...1500)

`bb({eyes:"wat_2"});`

b: えっ?

`hong({body:"phone1", eyes:"anger", mouth:"anger"});`

h: 私はあの招待に はい って答える。

{{if _.act1g=="go"}}
h: あんたが行かせたいからじゃなくて、*私* が行きたいから行く。
{{/if}}

{{if _.act1g=="dont"}}
h: あんたが行かせたくないから、私は行く。
{{/if}}

```
hong({body:"putaway"});
sfx("rustle");
```

h: あんたは、私をコントロールできないから。

```
sfx("rustle2");
hong({body:"0_sammich", eyes:"0_annoyed", mouth:"0_neutral"});
```

h: じゃあこの ^くそ^ 平和の中でこのおいしいサンドウィッチを食べさして。

`hong({body:"2_sammich_eat"});`

(...601)

```
sfx("sandwich");
hong({body:"2_sammich_eaten", eyes:"0_lookaway", mouth:"0_chew1"})
```

(...601)

```
bb({body:"normal", eyes:"uncertain", mouth:"shut"});
Game.OVERRIDE_TEXT_SPEED = 0.5;
```

b: ...

```
bb({eyes:"normal_right"});
Game.OVERRIDE_TEXT_SPEED = 1;
```

b: ...

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 4;
```

b: ..................

(...500)

`bb({mouth:"normal"});`

[あああっっ俺ら死んじゃうううう](#act1h_death) `Game.OVERRIDE_CHOICE_LINE = true;`

[あああっっみんな俺らのこと嫌ってるうううう](#act1h_loneliness) `Game.OVERRIDE_CHOICE_LINE = true;`

[あああっっ俺らダメダメ人間だああああ](#act1h_worthless) `Game.OVERRIDE_CHOICE_LINE = true;`

# act1h_death

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: あああっっ俺ら死んじゃうううううううっっっ

```
hong({body:"3_defeated1"});
attack("100p", "harm");
```

(...2500)

(#act1i)

# act1h_loneliness

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: あああっっみんな俺らのこと嫌ってるうううううっっっ

```
hong({body:"3_defeated1"});
attack("100p", "alone");
```

(...2500)

(#act1i)

# act1h_worthless

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: あああっっ俺らダメダメ人間だあああああああっっっ

```
hong({body:"3_defeated1"});
attack("100p", "bad");
```

(...2500)

(#act1i)

# act1i

```
bb({mouth:"smile_lock", eyes:"smile", body:"normal"});
music('battle', {volume:0.5});
```

n: よくできました！！

(...500)

n: あなたは　ニンゲンの　身体的 + 社交的 + 道徳的な　ニーズを　無事に　守りました！！

n: ほらっ　見てください！　と〜っても　感謝してる　でしょう？！

(...500)

n: ニンゲンの　エネルギーを　ゼロに　したので、あなたは　ニンゲンを　直接　コントロール　できます！！

`bb({mouth:"smile", eyes:"normal"});`

n: 最後の　技を　選べ

`bb({mouth:"small_lock", eyes:"fear"});`

n: *トドメを　刺せ*

[{戦う：ストレスだらけのスマホを罰せよ！！}](#act1i_phone) `Game.OVERRIDE_CHOICE_LINE=true`

[{逃げる：体をボールにして泣け！！}](#act1i_cry) `Game.OVERRIDE_CHOICE_LINE=true`

# act1i_phone

`bb({mouth:"normal", eyes:"narrow"})`

b: 君のスマホは君に発作を起こしてたんだ！！

`bb({eyes:"anger"})`

b: ザッカーバーグとその一味が君の精神的健康をハイジャックしてベンチャーキャピタル・マネーに出資しちゃうよ！！

```
bb({body:"fear", eyes:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: スマホを罰するんだ！！ぶっ壊せ！！ぶっ殺せ！！

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "fight";
```

b: ぶっ殺せぶっ殺せぶっ殺せぶっ殺せぶっ殺せぶっ殺せぶっ殺せぶっ殺せぶっ殺せぶっ殺せぶっ殺せぶっ殺せぶっ殺せぶっ殺せぶっ殺せぶっ殺ーーー

(#act1j)

# act1i_cry

`bb({eyes:"fear", mouth:"normal"})`

b: この世界危険まみれなんだよ！！

```
bb({body:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: アルマジロみたいになれ！！ ボールみたいに丸まって自分を守れ！！

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "flight";
```

b: 丸まって泣け丸まって泣け丸まって泣け丸まって泣け丸まって泣け丸まって泣け丸まって泣け丸まって泣け丸まって泣け丸まって泣け丸まって泣ーーー

(#act1j)

# act1j

`SceneSetup.act1_outro()`

