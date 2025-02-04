---
layout: post
title: Sober Driver
tags: games geek en
original: guidi-tu
---
In 2023 I developed an app to tackle drunk driving.

This free app, which I called **Sober Driver** (**Guidi Tu** in the original Italian version), is used to designate, among a group of friends who went out drinking together, a sober driver who will have to drink only non-alcoholic beverages because they will be in charge of driving everyone back home. The choice, though, is made through a challenge to one of a dozen mini-games that combine cunning, dexterity and luck to varying degrees.

{% include itch.html widget="https://itch.io/embed/2505206?linkback=true&amp;bg_color=462550&amp;fg_color=ffffff&amp;link_color=391d42" url="https://maurovanetti.itch.io/tde" %}

The underlying idea comes from my clients, the [Cooperativa Alice](https://coopalice.net/) of Alba (CN) whom I met through the [Centro Steadycam](https://centrosteadycam.it/). Having won a state grant to combat alcoholism and the dangerous behaviours associated with this social scourge, they thought of creating a video game that could help promote the culture of the "designated sober driver", a little known concept in Italy but quite widespread in other countries. I then found the game design solution that would hopefully make the assignment of this duty engaging and playful.

The general mechanism to select who can drink, and who instead must remain sober to drive, is simple: a mini-game is chosen and whoever comes *last* will be the Designated Sober Driver. However, even the *first* will suffer a penalty: they will be declared the Designated Generous Benefactor, and will have to pay a forfeit in some way. For example, it can be ruled that the first must pay drinks to the last (non-alcoholic ones!), or fuel, or snacks to the whole group.

Using this mechanics, any game, even the simplest, becomes an exercise in *yomi*, a concept used in game design to indicate "mind reading" or rather the anticipation of the opponent's move. Think of when you play odds and evens: that's yomi. If I want to win, but not overwhelmingly, even an absurd game like "Who chooses the highest number wins" (any number) becomes non-trivial, because it becomes "The winners are all those who choose a number that is neither the lowest nor the highest among all the numbers chosen". I also like the concept underlying this mechanic -- it's like a race where no one wants to be left too far behind or make a breakaway, everyone stays more or less together; perhaps it says something about friendship (and perhaps also about alcoholism and road traffic).

The mini-games to choose from are generally inspired by "folk games", for example boules, battleship, and a noble relatives of the aforementioned odds and evens: rock-paper-scissors and the Italian morra -- I was surprised to discover that many Italians don't know what [morra](https://en.wikipedia.org/wiki/Morra_(game)) is, and confuse it with rock-paper-scissors that in Italian is known as "Chinese morra". But we also have mini-games that refer to traditional random-pick systems, so I called Guidi Tu a [virtual eeny-meeny-miny-moe](https://en.wikipedia.org/wiki/Eeny,_meeny,_miny,_moe): drawing the shortest stick, the aforementioned choosing a number. Since the ranking assignment mode refers to mind reading, I also added a game that is based on that in a more literal sense than battleship or rock-paper-scissors: I called it Telepathy and it looks like a dumber Wordle or a Mastermind, and to insist with occultism I also put in some references to the [ouija board](https://en.wikipedia.org/wiki/Ouija). About supernatural divination again, if we want to stick to folk games, it felt right to bring some reference to the Smorfia into the mini.games based on picking a number, and so I did (if you don't know what the Smorfia -- a kind of traditional dream-to-lotto-number conversion dictionary -- is, please translate this and you won't be disappointed: [Wikipedia article](https://it.wikipedia.org/wiki/La_smorfia)).

**Sober Driver** is a small declaration of love to the culture of play, a legacy that we carry with us straight from elementary-school schoolyards.

We made it using Flutter Flame, [the code is open source](https://github.com/maurovanetti/guidi-tu/) and it's free software. I switched to the plural because the collaboration of the brilliant artist and designer **Jacopo Rovida** was fundamental, first of all in giving the game a colourful and wonderfully childish look and feel, but also in correcting many design choices with a precious work of testing and advice that revolutionised both the original list of mini-games I had in mind and a myriad of UX aspects. Although constructed as an app rather than a video game as commonly understood, I tried to emphasise the odd and playful aspects directly inserted in the UI; with a certain pride I must say that the rising bubbles are wholly my work.

At the end of 2024 the app was localized by me in English, another interesting experience for the non-obvious choices I found myself facing, starting from the title; in Italian "Guidi Tu" means "You Drive", but the reversal of verb and pronoun stresses that it's you who drives and nobody else. I couldn't fathom a way to convey the same feeling in English and opted for **Sober Driver**: a soberer solution.

<a href='https://play.google.com/store/apps/details?id=net.coopalice.guiditu'>
<img alt='Get it on Google Play' src='https://github.com/maurovanetti/guidi-tu/blob/main/extra/readme/get-it-on-google-play.png?raw=true' style="height: 82px;"/></a>

<a href="https://apps.apple.com/it/app/guidi-tu/id6476491805?itscg=30200&itsct=apps_box_badge&mttnsubad=6476491805" style="display: inline-block;">
<img src="https://toolbox.marketingtools.apple.com/api/v2/badges/download-on-the-app-store/black/en-us?releaseDate=1706659200" alt="Download on the App Store" style="width: 246px; height: 82px; vertical-align: middle; object-fit: contain;" /></a>

<a href='https://url.cloud.huawei.com/pgR2uPpQTS?shareTo=qrcode'>
<img alt='Explore it on AppGallery' src='https://github.com/maurovanetti/guidi-tu/blob/main/extra/readme/explore-it-on-app-gallery.png?raw=true' style="height: 82px;"/>
</a>