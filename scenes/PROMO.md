# intro

`SceneSetup.intro();`

# intro-play-button

(...51)

[プレイ！](#intro-start) `publish("intro-to-game-1"); Game.OVERRIDE_CHOICE_LINE=true;`

# intro-start

(...500)

`clearText()`

n3: さて、始める前に、どんな風に読みたい？

`publish("show_options_bottom")`

# intro-start-2

n3: じゃあ、物語を始めよう…

```
publish("hide_tabs");
clearText();
```

(...1000)

`publish("intro-to-game-2")`

n2: これは人間だ

(...600)

`clearText()`

(...300)

`publish("intro-to-game-3")`

# act1

```
SceneSetup.act1();
publish("hide_tabs");
music('battle', {volume:0.5});
```

(...300)

n: そして、これがその人間の不安だ

n: _あなた_ が不安そのものだ

(#act1_normal)


# act1_normal

```
hong({body:"putaway"});
sfx("rustle");
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: いやいや、聞かない聞かない。スマホでも見よ。

```
sfx("rustle2");
hong({body:"phone1", mouth:"neutral", eyes:"neutral"})
```

n: あなたの仕事は人間を*危険*から守ること

`bb({eyes:"look", mouth:"small_lock", body:"fear"})`

b: あっ！またTwitterでダラダラスクロールしてる！

```
bb({eyes:"normal", mouth:"normal", body:"normal"});
hong({eyes:"annoyed"});
```

h: だから自分の気持ちとじっくり向き合わないのかな、不思議だよ。

`hong({eyes:"neutral"});`

n: 早く、*危険*を警告しろ！

```
bb({eyes:"look"});
```

[大変、あのひどいニュース記事を見て！](#act1d_news)

[大変、あのツイートってもしかして*私たち*のこと？](#act1d_subtweet)

[あ、猫がミルク飲んでるGIFだ](#act1d_milk)

# act1d_milk

`hong({mouth:"smile", eyes:"surprise"});`

h: あははかわい、って――

```
hong({mouth:"shock", eyes:"shock"});
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.8;
```

b: 猫はミルクを消化できないのに、動物虐待を楽しんでる私たちって最低な人間じゃないか！

(...200)

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
attack("20p", "bad");
publish("hp_show");
```



