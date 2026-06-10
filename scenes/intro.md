intro

SceneSetup.intro();

intro-play-button

(…51)

_.PLAYED_BEFORE = !!window.localStorage.continueChapter;

{{if !_.PLAYED_BEFORE}}
Game.OVERRIDE_FONT_SIZE=30;
{{/if}}

{{if !_.PLAYED_BEFORE}}
#play1# はじめる！ #play2# publish("intro-to-game-1"); Game.OVERRIDE_CHOICE_LINE=true;
{{/if}}

{{if _.PLAYED_BEFORE && window.localStorage.continueChapter==“act2”}}
つづきから: パーティー publish("LOAD_GAME", ["act2"]); Game.OVERRIDE_CHOICE_LINE=true;
{{/if}}

{{if _.PLAYED_BEFORE && window.localStorage.continueChapter==“act3”}}
つづきから: もうひとつのパーティー publish("LOAD_GAME", ["act3"]); Game.OVERRIDE_CHOICE_LINE=true;
{{/if}}

{{if _.PLAYED_BEFORE && window.localStorage.continueChapter==“act4”}}
つづきから: もうひとつのサンドイッチ publish("LOAD_GAME", ["act4"]); Game.OVERRIDE_CHOICE_LINE=true;
{{/if}}

{{if _.PLAYED_BEFORE && window.localStorage.continueChapter==“replay”}}
Game.OVERRIDE_FONT_SIZE=30;
{{/if}}

{{if _.PLAYED_BEFORE && window.localStorage.continueChapter==“replay”}}
#play1# もう一度！ #play2# publish("intro-to-game-1"); Game.OVERRIDE_CHOICE_LINE=true;
{{/if}}

{{if _.PLAYED_BEFORE}}
チャプター選択 Game.OVERRIDE_CHOICE_LINE=true;
{{/if}}

(注意事項) Game.OVERRIDE_CHOICE_LINE=true; publish('show_cn');

chapter-select

publish("HACK_chselect");

I. サンドイッチ publish("HACK_chselect_end"); publish("intro-to-game-1"); Game.OVERRIDE_CHOICE_LINE=true;

II. パーティー publish("HACK_chselect_end"); publish("LOAD_GAME", ["act2"]); Game.OVERRIDE_CHOICE_LINE=true;

{{if window.localStorage.act3}}
III. もうひとつのパーティー publish("HACK_chselect_end"); publish("LOAD_GAME", ["act3"]); Game.OVERRIDE_CHOICE_LINE=true;
{{/if}}

{{if !window.localStorage.act3}}
III. もうひとつのパーティー
{{/if}}

{{if window.localStorage.act4}}
IV. もうひとつのサンドイッチ publish("HACK_chselect_end"); publish("LOAD_GAME", ["act4"]); Game.OVERRIDE_CHOICE_LINE=true;
{{/if}}

{{if !window.localStorage.act4}}
IV. もうひとつのサンドイッチ
{{/if}}

{{if window.localStorage.credits}}
V. クレジット publish("HACK_chselect_end"); Game.OVERRIDE_CHOICE_LINE=true;
{{/if}}

{{if !window.localStorage.credits}}
V. クレジット
{{/if}}

(タイトル画面) publish("HACK_chselect_end"); Game.OVERRIDE_CHOICE_LINE=true;

to-credits

stopAllSounds();

(…101)

(#credits)

intro-start

(…500)

clearText()

n3: ようこそ！ これは「ゲーム」というより、インタラクティブな物語だ。

n3: つまり文章を読むのがメインってこと！ 読むの嫌いなら……今のうちに逃げとけ！

n3: さて、始める前に―― 君 はどんな感じで読みたい？

publish("show_options_bottom")

intro-start-2

n3: よし！ 安心しろ、下の歯車アイコンからいつでも設定を変えられるぞ。

n3: それと、このゲームは各チャプターごとに自動セーブされる！

n3: それじゃあ、物語を始めよう……

clearText()

(…1000)

publish("intro-to-game-2")

n2: これがニンゲンだ

(…600)

clearText()

(…300)

publish("intro-to-game-3")
