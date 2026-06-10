# intro

`SceneSetup.intro();`

# intro-play-button

(...51)


_.PLAYED_BEFORE = !!window.localStorage.continueChapter;


{{if !_.PLAYED_BEFORE}}
`Game.OVERRIDE_FONT_SIZE=30;`
{{/if}}

{{if !_.PLAYED_BEFORE}}
[#play1# はじめる！ #play2#](#intro-start) `publish("intro-to-game-1"); Game.OVERRIDE_CHOICE_LINE=true;`
{{/if}}

{{if _.PLAYED_BEFORE && window.localStorage.continueChapter=="act2"}}
[_つづきから_: パーティー](#act2) `publish("LOAD_GAME", ["act2"]); Game.OVERRIDE_CHOICE_LINE=true;`
{{/if}}

{{if _.PLAYED_BEFORE && window.localStorage.continueChapter=="act3"}}
[_つづきから_: もうひとつのパーティー](#act3) `publish("LOAD_GAME", ["act3"]); Game.OVERRIDE_CHOICE_LINE=true;`
{{/if}}

{{if _.PLAYED_BEFORE && window.localStorage.continueChapter=="act4"}}
[_つづきから_: もうひとつのサンドイッチ](#act4) `publish("LOAD_GAME", ["act4"]); Game.OVERRIDE_CHOICE_LINE=true;`
{{/if}}

{{if _.PLAYED_BEFORE && window.localStorage.continueChapter=="replay"}}
`Game.OVERRIDE_FONT_SIZE=30;`
{{/if}}

{{if _.PLAYED_BEFORE && window.localStorage.continueChapter=="replay"}}
[#play1# もう一度！ #play2#](#intro-start) `publish("intro-to-game-1"); Game.OVERRIDE_CHOICE_LINE=true;`
{{/if}}

{{if _.PLAYED_BEFORE}}
[チャプター選択](#chapter-select) `Game.OVERRIDE_CHOICE_LINE=true;`
{{/if}}

[(注意事項)](#intro-play-button) `Game.OVERRIDE_CHOICE_LINE=true; publish('show_cn');`

# chapter-select

`publish("HACK_chselect");`

[I. サンドイッチ](#intro-start) `publish("HACK_chselect_end"); publish("intro-to-game-1"); Game.OVERRIDE_CHOICE_LINE=true;`

[II. パーティー](#act2) `publish("HACK_chselect_end"); publish("LOAD_GAME", ["act2"]); Game.OVERRIDE_CHOICE_LINE=true;`

{{if window.localStorage.act3}}
[III. もうひとつのパーティー](#act3) `publish("HACK_chselect_end"); publish("LOAD_GAME", ["act3"]); Game.OVERRIDE_CHOICE_LINE=true;`
{{/if}}

{{if !window.localStorage.act3}}
[III. もうひとつのパーティー]()
{{/if}}

{{if window.localStorage.act4}}
[IV. もうひとつのサンドイッチ](#act4) `publish("HACK_chselect_end"); publish("LOAD_GAME", ["act4"]); Game.OVERRIDE_CHOICE_LINE=true;`
{{/if}}

{{if !window.localStorage.act4}}
[IV. もうひとつのサンドイッチ]()
{{/if}}

{{if window.localStorage.credits}}
[V. クレジット](#to-credits) `publish("HACK_chselect_end"); Game.OVERRIDE_CHOICE_LINE=true;`
{{/if}}

{{if !window.localStorage.credits}}
[V. クレジット]()
{{/if}}

[(タイトル画面)](#intro-play-button) `publish("HACK_chselect_end"); Game.OVERRIDE_CHOICE_LINE=true;`

# to-credits

`stopAllSounds();`

(...101)

(#credits)

# intro-start

(...500)

`clearText()`

n3: ようこそ！ これは「ゲーム」というより、インタラクティブな物語だ。

n3: 読むのが好きだといいな！ じゃあ、始める前に―― *君* はどんな感じで読みたい？

`publish("show_options_bottom")`

# intro-start-2

n3: よし！ 安心しろ、下の⚙アイコンからいつでも設定を変えられるぞ。

n3: それと、このゲームは各チャプターごとに自動セーブされる！

n3: それじゃあ、物語を始めよう……

`clearText()`

(...1000)

`publish("intro-to-game-2")`

n2: これがニンゲンだ

(...600)

`clearText()`

(...300)

`publish("intro-to-game-3")`

`publish("intro-to-game-3")`
