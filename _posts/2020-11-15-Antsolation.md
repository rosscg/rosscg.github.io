---
layout: post
title: Antsolation
image:  /images/posts/antsolation-thumb.png
tags:   gamedev
excerpt: Virtual ant farm game. Made at Oxford Hackathon 2020.
---
Create a virtual ant farm and compete with your friends.

<table><tr>
  <td><p><video src="/images/posts/antsolation-gameplay.mov" width="640" autoplay muted loop/></p></td>

  <td style="width: 10px;"></td>

  <td style="vertical-align: middle;">
    <b><p><a href="{{ site.baseurl }}/apps/Antsolation.html"  target="_blank">Launch in Browser</a></p>

    <p><a href="https://github.com/rosscg/Antsolation/releases"  target="_blank">Download for Desktop (Windows/MacOS)</a></p></b>

    <p>Note: Multiplayer (i.e. importing and exporting ant colonies) is not supported for the browser version.</p>
  </td>
</tr></table>

### Motivation:
The motivation for this game was to develop a game which fostered [tend and befriend](https://en.wikipedia.org/wiki/Tend_and_befriend) behaviour; giving players something to take care of during periods of social isolation. The game is designed to require infrequent input from the user, simulating an ecosystem which the user can influence and observe.

The multiplayer aspect is designed to generate a feeling of presence from the other party in an asynchronous manner -- once a friend sends you their ant 'code', you can then play against their ants and discover their strategies over a long period of time without direct input from the friend. In this way, the presence of the friend can be felt throughout the day, as the two colonies of ants interact.

### Gameplay:
Ants periodically spawn and seek out nearby resources to harvest. Once their carrying capacity is reached, they will return to the nearest nest to deposit their resources. Upon spotting an enemy ant, they may choose to either attack or ignore them. Ants have limited vision, and will wander randomly until they find an item of interest. Once a nest reaches maturity and has enough food, it will spawn queens, who will create new nests. Ants can die from combat and old age.

The player can adjust the stats of newborn ants by opening the menu in the top left corner. Once a player is happy with their species of ant, they can export their genetics strain to the server. By passing their unique player ID on to a friend, the friend is then able to import the player's ants into their own game as the red species. In this way, players are able to compete with each other asynchronously.

The game is designed to be slow paced, supporting a contemplative play style.

<table><tr><td>
<iframe width="640" height="360" src="https://www.youtube.com/embed/y299m0jmlbo" frameborder="0"  style="float: left;margin-left: 6px; margin-right: 22px; margin-top: 0px;" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</td></tr></table>

*Antsolation* is an app built for the 2020 Oxford Hackathon over 24 hours. As such it is very much an alpha.

[Link to DevPost.](https://devpost.com/software/antsolation)

[Link to Github repository.](https://github.com/rosscg/Antsolation)

The current build has not been optimised for or tested on mobile devices.

### Development Notes

#### Ant AI
The game is built upon independent units of AI which control each ant and do not share direct communication between instances. Each ant unit receives information using local senses, thus the game intelligence is modelled on real ant colony collective intelligence.

An ant can 'see' a short radius around itself and makes decisions based on its individual priorities. These may include immediate needs such as thirst and fatigue, or overall colony needs (as the ant currently understands them).

<p><video src="/images/posts/antsolation-prototype.mov" width="640" autoplay muted loop/></p>

#### Colony Customisation
<img src="/images/posts/antsolation-build.png" alt="Colony customisation interface" width="400"/>


#### Multiplayer:
> Limited time, so used simple webserver from dept
> could only run safePerl, so limited DB functionality

<img src="/images/posts/antsolation-perl-save.png" alt="Perl code to save" width="400"/>




`{"player_id":5119,"Nest Range":300,"Courtiers":2,"Ex. Food":0,"Speed":0,"Vision":0,"Damage":0,"Health":0,"Carrying":0,"Lifespan":0,"Scouting":0,"Aggressive":0}`

[<img src="/images/posts/antsolation.png" alt="Antsolation App" width="800"/>]({{ site.baseurl }}/apps/Antsolation.html){:target="_blank"}
