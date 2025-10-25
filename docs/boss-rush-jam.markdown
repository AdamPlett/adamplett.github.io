---
layout: single
title: "Boss Rush Game Jam"
permalink: /boss-rush-jam/
---
Lumenimpetus was an entry for the 2024 Boss Rush Game Jam. It was a collaborative effort between me and two other friends, made in Unity. The theme was exchange. Our take was a movement based first person hack and slash/shooter, where you exchanged abilities with each boss you defeated.
I mainly focused on level design, enviromental scripting, debugging, UI scripting/design, and sound. 

## Breakable Objects
One of the first thing I created was a modular breakable object script. Breakable objects can be destroyed by another object calling its breakObject function (i.e. a projectile). Objects can also be destroyed if they have supports but all of them have been destroyed.
Using a fractured model you can set the relative force that the pieces will fly apart at. Lastly you can add any particle systems or objects you might want to spawn.
<video width="720" height="480" autoplay loop muted>
  <source src="/assets/images/BreakableObjectPillar.mp4" type="video/mp4">
</video>
<video width="720" height="480" autoplay loop muted>
  <source src="/assets/images/BreakableObjectSmoke.mp4" type="video/mp4">
</video>

## Arena Design
The first boss's ability is a grapple, that he can use to pull the player in for melees, or grapple away for ranged attacks. In the second phase the boss would ocassionally grapple up to one of the higher platforms and we wanted the player to have to complete a small puzzle or challenge to be able to reach them. So I played around with a couple ways of accomplishing this.
First I made a way for the player to bring down the upper platform by destorying it supports but it was just too buggy. Next I made a wallrunning/parkour segment but it was just too noisy and obstructed a lot of view. Lastly I made it so that the player could guide the bosses projectile into the pillars to destroy them, and create small sections where the player can wallrun up, off to the sides of the arena.
<video width="720" height="480" autoplay loop muted>
  <source src="/assets/images/BreakableObjectPlatformPhysicsReframe.mov" type="video/mp4">
</video>

Physics Based
<video width="720" height="480" autoplay loop muted>
  <source src="/assets/images/ParkourWDashReframe.mov" type="video/mp4">
</video>

Parkour Based
<video width="720" height="480" autoplay loop muted>
  <source src="/assets/images/BreakableObjectWallrunFinal.mp4" type="video/mp4">
</video>

Breakable Object and Wallrun

The second boss uses portals to teleport away and the player must platform assisted by their grapple to chase down the boss. The boss also uses portals placed around the map to shoot her lasers through to create hazards.

[comment]: # (Portals and lasers video)
<iframe src="https://www.youtube.com/embed/fE0g_AD0gfQ?controls=0&mute=1&showinfo=0&rel=0&autoplay=1&loop=1&playlist=fE0g_AD0gfQ" width="560" height="315" frameborder="0" allowfullscreen></iframe>

[comment]: # (Grappling and platforming video after boss TPs away)
I also created a simple tutorial so the players can get down the basics.
<video width="720" height="480" autoplay loop muted>
  <source src="/assets/images/BossRushTutorialReframed.mp4" type="video/mp4">
</video>

## UI and Sound
I implemented all of the UI and Sound.

I also made all the functionality for the settings, menus/pause, HUD, and any other UI. 
<video width="720" height="480" autoplay loop muted>
  <source src="/assets/images/BossRushMainMenu.mp4" type="video/mp4">
</video>

The hud consisted of a health bar and some animated icons to tell you when you have your ranged attack or dash available and the boss health bar.
<video width="720" height="480" autoplay loop muted>
  <source src="/assets/images/BossRushHUD.mp4" type="video/mp4">
</video>

Dymanic crosshair when grappling, depending on if it was successful or not.
<video width="720" height="480" autoplay loop muted>
  <source src="/assets/images/BossRushGrappleFail.mp4" type="video/mp4">
</video>
<video width="720" height="480" autoplay loop muted>
  <source src="/assets/images/BossRushGrapple.mp4" type="video/mp4">
</video>

For fun after the boss jam I made a loading/transition screen for between levels.
<video width="720" height="480" autoplay loop muted>
  <source src="/assets/images/LoadingScreenCrop.mp4" type="video/mp4">
</video>

## Pathing algorithim
Also after the game jam I implemented an a* pathing algorithim that traverses octrees, to help with pathing for homing projectiles or enemy movement. 
{% include figure popup=true image_path="/assets/images/octrees.png" %}
<video width="720" height="480" autoplay loop muted>
  <source src="/assets/images/astar.mp4" type="video/mp4">
</video>
