# intro

`SceneSetup.intro();`

# intro-play-button

(...51)

[PLAY!](#intro-start) `publish("intro-to-game-1"); Game.OVERRIDE_CHOICE_LINE=true;`

# intro-start

(...500)

`clearText()`

n3: ?אז לפני שנתחיל, איך *אתם* רוצים לקרוא

`publish("show_options_bottom")`

# intro-start-2

n3: ...עכשיו, בואו נתחיל בסיפור שלנו

```
publish("hide_tabs");
clearText();
```

(...1000)

`publish("intro-to-game-2")`

n2: זה בן אדם

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

n: וזאת החרדה של בן האדם

n: _אתם_ החרדה

(#act1_normal)


# act1_normal

```
hong({body:"putaway"});
sfx("rustle");
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: .לא, לא, לא, אני לא מקשיב. אני אבדוק את הטלפון שלי 

```
sfx("rustle2");
hong({body:"phone1", mouth:"neutral", eyes:"neutral"})
```

n: המטרה שלכם היא להגן על בן האדם שלכם *מסכנה*

`bb({eyes:"look", mouth:"small_lock", body:"fear"})`

b: !אוי לא! אתה מבזבז את החיים שלך בטוויטר! שוב

```
bb({eyes:"normal", mouth:"normal", body:"normal"});
hong({eyes:"annoyed"});
```

h: כן, אני *תוהה* למה אני לא יושב ומקשיב למחשבות שלי יותר פעמים

`hong({eyes:"neutral"});`

n: !מהר, תזהירו אותו מפני *סכנה*

```
bb({eyes:"look"});
```

[!אוי לא, תראה את סיפור החדשות הנוראי הזה](#act1d_news)

[אוי לא, האם הציוץ הזה בעצם *עלינו?*](#act1d_subtweet)

[הי, הנה גיף של חתול שותה חלב](#act1d_milk)

# act1d_milk

`hong({mouth:"smile", eyes:"surprise"});`

h: -- אה כן זה חמוד, אני 

```
hong({mouth:"shock", eyes:"shock"});
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.8;
```

b: חתולים לא יכולים לעכל חלב ואנחנו אנשים נוראיים שנהנים מהתעללות בחיות 

(...200)

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
attack("20p", "bad");
publish("hp_show");
```



