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

## UI

## Pathing algorithim
After the game jam I created an a* pathing algorithim that traverses octrees, pathing for projectiles or enemy movement. 