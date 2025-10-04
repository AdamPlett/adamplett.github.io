---
layout: single
title: "Boss Rush Game Jam"
permalink: /boss-rush-jam/
---
Lumenimpetus was an entry for the 2024 Boss Rush Game Jam, that some friends and I made in Unity. The theme was exchange. Our take was a movement based first person hack and slash/shooter, where you exchanged abilities with each boss you defeated.
I focused on level design, enviromental scripting, UI design/scripting. 

## Breakable Objects
I created a verastile breakable object script. Breakable objects can be destroyed by another object calling its breakObject function (i.e. a projectile). Objects can also be destroyed if they have supports but all of them have been destroyed.
Using a fractured model you can set the relative force that the pieces will fly apart at. Lastly you can add any particle systems or objects you might want to spawn.
<video width="720" height="480" autoplay loop muted>
  <source src="/assets/images/BreakableObjectPillar.mp4" type="video/mp4">
</video>


## Arena Design
The first boss fight was designed with two stages. The second consiting of the boss ocassionally grappling up to a higher platform that the player would have to complete a small puzzle or challenge to be able to reach. I played around with a couple ways of accomplishing this.
First I made a way for the player to bring down the upper platform by destorying it supports but it was just too buggy. Next I made a wallrunning/parkour segment but it was just too noisy and obstructed a lot of view. Lastly I made it so that the player could guide the bosses projectile into the pillars to destroy them, and create wallruns up, off to the sides of the arena.
<video width="720" height="480" autoplay loop muted>
  <source src="/assets/images/BreakableObjectPlatformPhysics.mp4" type="video/mp4">
</video>
<video width="720" height="480" autoplay loop muted>
  <source src="/assets/images/ParkourWDash.mp4" type="video/mp4">
</video>
<video width="720" height="480" autoplay loop muted>
  <source src="/assets/images/BreakableObjectWallrun1.mp4" type="video/mp4">
</video>
## UI

## Pathing algorithim
After the game jam I created an a* pathing algorithim that traverses octrees, to help with pathing for projectiles or enemy movement. 
{% include figure popup=true image_path="/assets/images/octrees.png" %}
<video width="720" height="480" autoplay loop muted>
  <source src="/assets/images/astar.mp4" type="video/mp4">
</video>
