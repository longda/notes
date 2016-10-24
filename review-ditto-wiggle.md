 <img src="https://raw.githubusercontent.com/longda/notes/master/img/wiggle-wobble.gif" alt="wiggle wobble" />

## Review: Mattias Dittrich (Ditto) - Make It Wiggle (or How to Make Cool Art with No Talent)

[Link to talk](https://www.youtube.com/watch?v=7-fUvFkPngI)

[![video of talk](http://img.youtube.com/vi/7-fUvFkPngI/0.jpg)](http://www.youtube.com/watch?v=7-fUvFkPngI)
<iframe width="560" height="315" src="https://www.youtube.com/embed/7-fUvFkPngI" frameborder="0" allowfullscreen></iframe>

[Make it wiggle](https://ditto.itch.io/makeitwiggle)
[Ditto @ www](http://www.matthiasdittrich.com/)
[Ditto @ Twitter](https://twitter.com/dittomat)
[Ditto @ itch.io](https://ditto.itch.io/)
[Ditto @ Cartridge](https://cartrdge.com/ditto)


### Consistency
  Same level of detail.  Low fidelity.
  

### Wiggle
  Draw the same frame 4 times.  e.g. draw a tree four times.
  When animated, each frame will be slightly different, bringing alive the tree with the wiggle effect.
  
  <img src="https://cdn.rawgit.com/longda/notes/master/img/ditto-wiggle-tree.png" alt="wiggle tree" />
  
    + Trees
    + Players
    + Squares/Obstacles
    + Platforms
    + Grass
    + Vegatation
    + Items
    + Clouds
  
  Game Demo
  
    + Ground
    + Player - can move behind trees
    + Forest
    + Color - lower saturation (80%)
    + Variation (flip, color, scale of objects, e.g. trees)
    + Stars
    + Details
    + 2nd color blend: sprite of transparent color and slap over the others (roll through in editor tool: blue, purple)
    + Wiggle everthing!
    + Clouds
    + Grass
    + Rocks
    + Moon + face
    + Code Cheat: animate star movement: pos = Vector2(Sin(deltaTime), Cosine(deltaTime)) [11:50](https://youtu.be/7-fUvFkPngI?t=11m50s)
    + Wobble! e.g. trees, grass: tree.rot (angle) * sin(deltaTime) * wiggle (each time walk into tree, wiggle is set to random number above) - goes back and forth with the sine wave. [slide 12/22]
    + Sprite stretch: when turning around, jumping: scale is 1,1 (normal) use lerp when jump, set x < 1, when land x > 1, then go back to normal.  [slide 14/22]
    + Outlines: technique: drawing the same sprite, different color, at an offset 8 times (n, s, e, w, ne, se, sw, nw) [slide 16/22]
    + Camera shake [slie 20/22]
    + 
    

### Code for Scripting Cheats

```javascript
//moving stars:
pos = vec2( sin(time), cos(time) );

//pushing trees:
rot = sin(time) * wiggle;
wiggle *= 0.95;

//sprite stretching: 
scale = vec2(x, y);
x = lerp(x, 1, 0.1);
y = lerp(y, 1, 0.1);
```


