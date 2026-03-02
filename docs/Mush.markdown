---
layout: single
classes: wide
title: "Mush"
permalink: /mush/
excerpt: "2D platformer Vertical Slice Demo"
header:
  overlay_image: /assets/images/mush_GameplayHeaderResized.png
  overlay_filter: 0.35
---
Mush was my senior project in Spring 2025. It is a vertical slice of an action platformer created in Unity. I created all the assets (Scripts, SFX, sprites, animations, etc.). My major focus was to create a solid foundation (modular and easy to write code, Scriptable objects for convenient and quick game design, "paintable levels', a highly customizable and good feeling jump mechanic, and documentation).
## Coding Architecture for character systems
{% include figure popup=true image_path="/assets/images/mush_coding.png" %}

I used loose coupling to allow for modular scripts. It takes longer to set up but allows for rapid iteration and creation of new assets based on good architecture. You can iterate on one section without messing up the others and would allow for multiple people to work on seperate scripts at once. Finally it localizes bugs and makes them easier to squash.
{% include figure popup=true image_path="assets/images/mush_coding_pics.png" %}

## Making The Designers Job Easier
{% include figure popup=true image_path="/assets/images/mush_stats_doubleJump.gif" caption="Changing the amount of double jumps" %}{: .align-left}
{% include figure popup=true image_path="/assets/images/mush_stats_highJump.gif" caption="Changing jump height" %}{: .align-left}
{% include figure popup=true image_path="/assets/images/mush_SO_stats.png" caption="Changable stats" %}{: .align-right}
I designed the movement to be completely customizable with stats (Converted things like intial jump speed to jump height for easier comprehension). Because they use scriptable objects, designers can edit them in and out of play mode and they will save between.
{: .text-right}
{:style="clear: right"}
<br><br>
To make debugging and designing faster, I also created scriptable object controllers so that designers can easily switch between controlling players/enemies or having AI control them.
{: .text-center}
{% include figure popup=true image_path="/assets/images/mush_inputController.png" caption=" The abstract Input Controller class" %}{: .align-center}
{% include figure popup=true image_path="/assets/images/mush_controllerClass.png" caption="The Controller class holds a null instance of an input controller, so that the designer can change it in the unity editor and while in play mode" %}{: .align-center}
{% include figure popup=true image_path="/assets/images/mush_code_controller.png" caption="The Player Controller class, derived from the input controller class, that takes in input from the user" %}
{% include figure popup=true image_path="/assets/images/mush_AIController.png" caption="A very simple AI controller class that makes enemies or players move right and jump and is also derived from the input controller class" %}
{% include figure popup=true image_path="/assets/images/mush_controllers.gif" caption="Switching between player and AI input controllers in unity play mode" %}{: .align-center}
You can find the rest of the my scripts on my [Github](https://github.com/AdamPlett/Mush/tree/main/Assets/Scripts).

## Paintable Level Design
{% include figure popup=true image_path="/assets/images/mush_tiles_paint.gif" %}{: .align-center} 
{% include figure popup=true image_path="assets/images/mush_tiles_setup.gif" %}{: .align-left}
I created a set of tiles, that when added to a rule tile in unity, allows you to "paint" level design. The configuration of the rule tile automatically selects the right tile for the position and retroactively change previous tiles to align with new ones. This allows designers to focus on building the flow of the level rather wasting time on placing the correct tiles
{: text-right}

## Item Pickups
{: .text-center}
{% include figure popup=true image_path="/assets/images/mush_code_bubble.png" %}
<iframe src="https://www.youtube.com/embed/iufBszNBXFs?controls=0&mute=1&showinfo=0&rel=0&autoplay=1&loop=1&playlist=iufBszNBXFs" width="560" height="315" frameborder="0" allowfullscreen></iframe>

## Gameplay
<video width="720" height="480" controls="controls">
  <source src="/assets/images/mush_gameplay.mp4" type="video/mp4">
</video>
