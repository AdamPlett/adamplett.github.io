---
layout: single
title: "Two Button Game Jam"
permalink: /2b-game-jam/
excerpt: "2D Horder shooter"
header:
  overlay_image: /assets/images/2BGameJamHeader.png
  overlay_filter: 0.225
---
Resist the Maelstrom was a game me and a couple of friends made for my first ever game jam. It was a week long with the parameters of making your game playable with only two buttons. It is a top down 2D horde shooter where you control a flying pirate ship and fight hordes of enemies to upgrade your aresnal of weaponry. You can use you main booster to fly around or let the recoil of your weaponry propel you as you add more and more firepower to your ship. For my portion I created all the enemies and powerups, their spawners, their pixel art, as well as the UI and implementing the audio for the game.

For both the enemies and powerups and their spawners I used an abstract class to inherit from and hold the base logic that they would all use and then used derived classes for each type of enemies, powerups, etc. to create their unique behaviors.

For example the slime class inherits from the abstract enemy class.
{% include figure popup=true image_path="/assets/images/2BGameJamEnemyScript.png" caption="The abstract enemy class with the base logic for all enemies" %}
{% include figure popup=true image_path="/assets/images/2BGameJamSlimeScript.png" caption="Some of the slime's unique behaviors" %}
Or the Eye's ranged attack
{% include figure popup=true image_path="/assets/images/2BGameJamEyeScript.png" caption="" %}
Then their stats can be changed in the editor
{% include figure popup=true image_path="/assets/images/2BGameJamSlimeUnity.png" caption="Slime Prefab" %}
{% include figure popup=true image_path="/assets/images/2BGameJamSlimeSpawnerUnity.png" caption="Slime Spawner Script" %}

You can find the rest of the scripts from the jam on my [Github page](https://github.com/AdamPlett/2ButtonGameJam/tree/main/Assets/Scripts).

You can try out the game on my [itch.io page](https://adamplett.itch.io/resist-the-maelstrom)! I recommend playing the normal mode as the maelstrom mode can be a bit buggy.

Below you can also find my sprite sheet for the enemies and powerups
{% include figure popup=true image_path="/assets/images/2BGameJamSprites.png" caption="Compliation of sprite sheets" %}