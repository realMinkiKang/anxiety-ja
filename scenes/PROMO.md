# intro

`SceneSetup.intro();`

# intro-play-button

(...51)

[PLAY!](#intro-start) `publish("intro-to-game-1"); Game.OVERRIDE_CHOICE_LINE=true;`

# intro-start

(...500)

`clearText()`

n3: そしたら始める前に、 *君* はこのお話をどんな風に読んで欲しい？

`publish("show_options_bottom")`

# intro-start-2

n3: それじゃあ、始めようか。。。

```
publish("hide_tabs");
clearText();
```

(...1000)

`publish("intro-to-game-2")`

n2: こいつ　は　ニンゲンだ

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

n: そして こいつ は ニンゲン の フアン　だ

n: _君_　は　フアン　だ

(#act1_normal)


# act1_normal

```
hong({body:"putaway"});
sfx("rustle");
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: アー　アーアー　キイテマセンー　もう　うるさいな。。。 携帯でも見とこ。

```
sfx("rustle2");
hong({body:"phone1", mouth:"neutral", eyes:"neutral"})
```

n: 君　の　目的　は　ニンゲン　を　*危険*　から　守る　ことだ

`bb({eyes:"look", mouth:"small_lock", body:"fear"})`

b: あっ！！　またまたツイッターで人生逃避してる！！　これで何回目？！
```
bb({eyes:"normal", mouth:"normal", body:"normal"});
hong({eyes:"annoyed"});
```

h: あーあ。。。なんで私ってもっと自分の感情の事ちゃんと聞かないんだろう。。。

`hong({eyes:"neutral"});`

n: ほらっ！！　早く *危険*　って　警告　してっ！！！！

```
bb({eyes:"look"});
```

[見ろ見ろ！！ こんな最悪なニュースが出てる！！](#act1d_news)

[待て！！ そのツイート *僕たち* のことじゃないか？！](#act1d_subtweet)

[おいっ 猫がミルクを飲んでるGIFがあるぞっ](#act1d_milk)

# act1d_milk

`hong({mouth:"smile", eyes:"surprise"});`

h: これ？そうだね、可愛いよね。 私ーーー

```
hong({mouth:"shock", eyes:"shock"});
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.8;
```

b: 猫はミルクを消化できねーんっだよ！！！ だから俺らは動物虐待を楽しんでいる　サイテーな　奴らなんだよ！！！

(...200)

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
attack("20p", "bad");
publish("hp_show");
```



