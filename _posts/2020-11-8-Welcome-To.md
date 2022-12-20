---
layout: post
title: \'Welcome To\' App
image:  /images/posts/welcome-to-thumb.png
tags:   gamedev
excerpt: Card drawing app for the board game 'Welcome To...'
---

<table><tr>
<td>
  <p><video src="/images/posts/welcome-to-demo.mp4" autoplay muted loop/></p>
</td>
<td style="width: 10px;"></td>
<td style="vertical-align: middle;">
  <p><i>'Welcome To...'</i> is a 'roll and write' game designed by Benoit Tupin, where players are architects in 1950s America competing to build the most desirable suburb.</p>

  <p>Roll and write games provide each player with a sheet of paper and pencil with which to record their decisions, and a set of variables are generated each turn. Traditionally, this is done with a set of dice (hence the term 'roll'); in 'Welcome To...' decks of cards are used instead. This app replicates the drawing of these cards.</p>

  <p align="center">
    <b><a href="{{ site.baseurl }}/apps/WelcomeTo.html" target="_blank">Launch Card Dealer for 'Welcome To'</a></b>
  </p>

  <p>The rules of the game can be found on <a href="https://boardgamegeek.com/filepage/162102/welcome-english-rules-20" target="_blank">BoardGameGeek</a> or the <a href="https://www.bluecocker.com/jeux/Welcome/Regles_fr&en.pdf" target="_blank">publisher's site</a>. A scoresheet is <a href="https://boardgamegeek.com/filepage/198138/welcome-entirely-fillable-player-sheet-pdf" target="_blank">available here</a> and can be printed or used directly within a web browser. A printer friendly version is <a href="https://boardgamegeek.com/filepage/182959/w2-score-sheet-printer-friendly" target="_blank">also available</a>. Scoresheet apps can be downloaded for <a href="https://apps.apple.com/us/app/welcome-to-your-perfect-home/id1358077007" target="_blank">iOS</a> or <a href="https://play.google.com/store/apps/details?id=com.bluecocker.welcome" target="_blank">Android</a> which handle the score calculations automatically.</p>

  <p>Tap the City Plan cards to mark them as 'approved' and remove the higher points value marker.</p>

</td>
</tr></table>

### Development Notes

The software is written in [Godot 3.1.2](https://godotengine.org/) using GDScript. Cards from the main deck are drawn randomly without replacement while the objective deck is drawn with replacement.
