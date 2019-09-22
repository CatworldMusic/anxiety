# intro

`SceneSetup.intro();`

# intro-play-button

(...51)

```
_.PLAYED_BEFORE = !!window.localStorage.continueChapter;
```

{{if !_.PLAYED_BEFORE}}
`Game.OVERRIDE_FONT_SIZE=30;`
{{/if}}

{{if !_.PLAYED_BEFORE}}
[#play1# !שחקו #play2#](#intro-start) `publish("intro-to-game-1"); Game.OVERRIDE_CHOICE_LINE=true;`
{{/if}}

{{if _.PLAYED_BEFORE && window.localStorage.continueChapter=="act2"}}
[_המשיכו: המסיבה](#act2) `publish("LOAD_GAME", ["act2"]); Game.OVERRIDE_CHOICE_LINE=true;`
{{/if}}

{{if _.PLAYED_BEFORE && window.localStorage.continueChapter=="act3"}}
[המשיכו: המסיבה האחרת](#act3) `publish("LOAD_GAME", ["act3"]); Game.OVERRIDE_CHOICE_LINE=true;`
{{/if}}

{{if _.PLAYED_BEFORE && window.localStorage.continueChapter=="act4"}}
[_המשיכו: הכריך האחר](#act4) `publish("LOAD_GAME", ["act4"]); Game.OVERRIDE_CHOICE_LINE=true;`
{{/if}}

{{if _.PLAYED_BEFORE && window.localStorage.continueChapter=="replay"}}
`Game.OVERRIDE_FONT_SIZE=30;`
{{/if}}

{{if _.PLAYED_BEFORE && window.localStorage.continueChapter=="replay"}}
[#play1# !שחקו שוב #play2#](#intro-start) `publish("intro-to-game-1"); Game.OVERRIDE_CHOICE_LINE=true;`
{{/if}}

{{if _.PLAYED_BEFORE}}
[בחרו פרק](#chapter-select) `Game.OVERRIDE_CHOICE_LINE=true;`
{{/if}}

[(אזהרות תוכן)](#intro-play-button) `Game.OVERRIDE_CHOICE_LINE=true; publish('show_cn');`

# chapter-select

`publish("HACK_chselect");`

[I. הכריך](#intro-start) `publish("HACK_chselect_end"); publish("intro-to-game-1"); Game.OVERRIDE_CHOICE_LINE=true;`

[II. המסיבה](#act2) `publish("HACK_chselect_end"); publish("LOAD_GAME", ["act2"]); Game.OVERRIDE_CHOICE_LINE=true;`

{{if window.localStorage.act3}}
[III. המסיבה האחרת](#act3) `publish("HACK_chselect_end"); publish("LOAD_GAME", ["act3"]); Game.OVERRIDE_CHOICE_LINE=true;`
{{/if}}

{{if !window.localStorage.act3}}
[III. המסיבה האחרת]()
{{/if}}

{{if window.localStorage.act4}}
[IV. הכריך האחר](#act4) `publish("HACK_chselect_end"); publish("LOAD_GAME", ["act4"]); Game.OVERRIDE_CHOICE_LINE=true;`
{{/if}}

{{if !window.localStorage.act4}}
[III. הכריך האחר]()
{{/if}}

{{if window.localStorage.credits}}
[V. קרדיטים](#to-credits) `publish("HACK_chselect_end"); Game.OVERRIDE_CHOICE_LINE=true;`
{{/if}}

{{if !window.localStorage.credits}}
[V. קרדיטים]()
{{/if}}

[(תפריט ראשי)](#intro-play-button) `publish("HACK_chselect_end"); Game.OVERRIDE_CHOICE_LINE=true;`

# to-credits

`stopAllSounds();`

(...101)

(#credits)

# intro-start

(...500)

`clearText()`

n3: !ברוכים הבאים! אז המשחק הזה הוא פחות *משחק* ויותר סיפור אינטראקטיבי. מקווים שאתם אוהבים לקרוא

n3: ?אז לפני שנתחיל, איך *בדיוק* תרצו לקרוא

`publish("show_options_bottom")`

# intro-start-2

 n3: .נהדר! הערה: אתם תמיד יכולים לשנות את ההגדרות הללו בעזרת האייקון של ה⚙ למטה. המשחק גם שומר את עצמו בסוף כל פרק

n3: ...עכשיו, בואו נתחיל בסיפורנו

`clearText()`

(...1000)

`publish("intro-to-game-2")`

n2: .זה בן אדם

(...600)

`clearText()`

(...300)

`publish("intro-to-game-3")`
