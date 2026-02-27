---
layout: single
title: "Two Button Game Jam"
permalink: /2b-game-jam/
---
Resist the Maelstrom was my first game jam that I did with a couple of friends. It was a week long with the parameters of making your game playable with only two buttons. For my portion I created all the enemies and powerups, their spawners, their pixel art, as well as the UI and implementing the audio for the game.

For both the enemies and powerups and their spawners I used an abstract class to inherit from and hold the base logic that they would all use and then used derived classes for each type of enemies, powerups, etc. to create their unique mechanics.

For example the slime class inherits from the abstract enemy class.
{% include figure popup=true image_path="/assets/images/2BGameJamEnemyScript.png" caption="The abstract enemy class with the base logic for all enemies" %}
{% include figure popup=true image_path="/assets/images/2BGameJamSlimeScript.png" caption="Some of the unique mechanics that the slime uses" %}

{% include figure popup=true image_path="/assets/images/2BGameJamSlimeUnity.png" caption="" %}
{% include figure popup=true image_path="/assets/images/2BGameJamSlimeSpawnerUnity.png" caption="" %}

You can find the rest of the scripts on my [Github](https://github.com/AdamPlett/2ButtonGameJam/tree/main/Assets/Scripts) page.

You can try out the game on my [itch.io page](https://adamplett.itch.io/resist-the-maelstrom). I recommend playing the normal mode as the maelstrom mode can be a bit buggy.