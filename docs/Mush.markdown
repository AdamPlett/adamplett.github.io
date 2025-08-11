---
layout: single
classes: wide
title: "Mush"
permalink: /mush/
gallery:
  - image_path: /assets/images/mush_stats_doubleJump.gif
  - image_path: /assets/images/mush_stats_highJump.gif
  - image_path: /assets/images/mush_SO_stats.png
gallery2:
  - image_path: /assets/images/mush_code_controller.png
  - image_path: /assets/images/mush_code_check.png
gallery3:
  - image_path: /assets/images/mush_inputController.png
  - image_path: /assets/images/mush_controllerClass.png
  - image_path: /assets/images/mush_code_controller.png
  - image_path: /assets/images/mush_AIController.png
---
Mush was my senior project in Spring 2025. It is a vertical slice of an action platformer created in Unity. I created all the assets (Scripts, SFX, sprites, animations, etc.). My major focus was to create a solid foundation (modular and easy to write code, Scriptable objects for convenient and quick game design, "paintable levels', and documentation)
## Coding Architecture
{% include figure popup=true image_path="/assets/images/mush_coding.png" %}

I used loose coupling to allow for modular scripts. It takes longer to set up but allows for rapid iteration and creation of new assets based on good architecture. You can iterate on one section without messing up the others and would allow for multiple people to work on seperate scripts at once. Finally it localizes bugs and makes them easier to squash.
![coding_controller](/assets/images/mush_code_controller.png)
![coding_check](/assets/images/mush_code_check.png)

## Making The Designers Job Easier
{% include gallery caption="I designed the movement to be completely customizable with stats (Converted things like jump speed to jump height for easier comprehension). They also use scriptable objects so that designers can edit the stats while in play mode in unity and the changes will save without needing to go back and forth" %}

To make debugging and designing faster, I also created scriptable object controllers so that designers can easily switch between controlling players/enemies or having AI control them.
{% include figure popup=true image_path="/assets/images/mush_inputController.png" caption=" The abstract Input Controller class" %}{: .align-center}
{% include figure popup=true image_path="/assets/images/mush_controllerClass.png" caption="The Controller class holds an instance of an input controller, so that the designer can change it while in play mode in unity" %}{: .align-center}
{% include figure popup=true image_path="/assets/images/mush_code_controller.png" caption="The Player Controller class that takes in input from the player and is derived from the input controller class" %}
{% include figure popup=true image_path="/assets/images/mush_AIController.png" caption="A very simple AI controller class that makes enemies or players move right and jump and is also derived from the input controller class" %}
{% include figure popup=true image_path="/assets/images/mush_controllers.gif" caption="Switching input controllers" %}{: .align-center}

## Paintable Level Design
{% include figure popup=true image_path="/assets/images/mush_tiles_paint.gif" %}{: .align-center} 
{% include figure popup=true image_path="assets/images/mush_tiles_setup.gif" %}{: .align-left}
I created a set of tiles, that when added to a rule tile in unity, allows you to "paint" level design. The configuration of the rule tile automatically selects the right tile for the position and retroactively change previous tiles to align with new ones. This allows designers to focus on building the flow of the level rather wasting time on placing the correct tiles
{: text-right}

## Powerups
{: .text-center}
{% include figure popup=true image_path="/assets/images/mush_code_bubble.png" %}

## Gameplay
<video width="720" height="480" controls="controls">
  <source src="/assets/images/mush_gameplay.mp4" type="video/mp4">
</video>
