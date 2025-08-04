---
layout: single
classes: wide
title: "Mush"
permalink: /mush/
gallery:
  - image_path: /assets/images/mush_stats_doubleJump.gif
  - image_path: /assets/images/mush_stats_highJump.gif
gallery2:
  - image_path: /assets/images/mush_tiles_paint.gif
  - image_path: /assets/images/mush_tiles_setup.gif
---
Mush was my senior project. It is a vertical slice of an action platformer. I created all the assets (Scripts, SFX, sprites, animations, etc.). My major focus was to create a solid foundation (modular and easy to write code, Scriptable objects for convenient and quick game design, "paintable levels', and documentation)
## Coding Architecture
![Coding Architecture](/assets/images/mush_coding.png)

I used loose coupling to allow for modular scripts. It takes longer to set up but allows for rapid iteration and creation of new assets based on good architecture. You can iterate on one section without messing up the others and would allow for multiple people to work on seperate scripts at once. Finally it localizes bugs and makes them easier to squash.

## Making The Designers Job Easier
{% include gallery caption="I designed the movement to be completely customizable with stats (Converted things like jump speed to jump height for easier comprehension). They also use scriptable objects so that designers can edit the stats while in play mode in unity and the changes will save without needing to go back and forth" %}
![Controllers](/assets/images/mush_controllers.gif){: .align-center}

In order to make debugging and designing faster, I also created scriptable objects so that designers can easily switch between controlling players/enemies or having AI control them.

## Paintable Level Design
![paintable](/assets/images/mush_tiles_paint.gif){: .align-left}          
![setup](/assets/images/mush_tiles_setup.gif){: .align-left} I created a set of tiles, that when added to a rule tile in unity, allows you to "paint" level design. The configuration of the rule tile automatically selects the right tile for the position and retroactively change previous tiles to align with new ones. This allows designers to focus on building the flow of the level rather wasting time on placing the correct tiles

## Gameplay
<video width="720" height="480" controls="controls">
  <source src="/assets/images/mush_gameplay.mp4" type="video/mp4">
</video>

<!---
{% include gallery id="gallery2" layout="third" %}
![doubleJump](/assets/images/mush_stats_doubleJump.gif){: align-left} 
![highJump](/assets/images/mush_stats_highJump.gif){: align-left}
--->