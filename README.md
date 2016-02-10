# The hoverFlow Plugin
JQuery plugin that prevents animation queue buildup in hover animations.

- **Author**: Ralf Stoltze
- **Souce**: http://www.2meter3.de/code/hoverFlow/
- **Version**: 1.00

The plugin honors a single mouseover/-out with a full animation cycle while preventing animation queue buildup.

A queued animation will only run if it corresponds with the current mouse position at "runtime". That is, a mouseover animation will only run if the mouse is currently over the element, and a mouseout animation will only run if the mouse is currently not over the element. Otherwise, the animation queue is empied.

### Usage
```
$('.example3 .anim_queue_example a')
  .hover(function(e) {
    $(this).hoverFlow(e.type, { left: 20 }, 'fast');
  }, function(e) {
    $(this).hoverFlow(e.type, { left: 0 }, 'fast');
  });
```


