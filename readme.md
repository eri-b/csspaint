## CSS-only Paint App

A simple paint app using a bit of CSS, and no javascript.


### Your HTML
```
<div class="canvas">
   <span></span>
   <span></span>
   ...
   <span></span>     
   <span></span>
</div>
```

### Your CSS
```
@keyframes hoverstyle {
  0% {background: white; }
  100% {background: black; } 
}
.canvas > span {
  animation-name: hoverstyle;
  animation-duration: 10ms;
  animation-play-state: paused;
  animation-fill-mode: both;
  padding: 3px;
}
.canvas > span:hover { animation-play-state: running; }
#canvas {
   display: flex;  
   flex-wrap: wrap;
   background:white;
   width:700px;
}
```
The span items are your pixels. When they're hovered, a transition is un-paused, causing the background of the pixel to move from whatever you set at 0% to whatever you set at 100% - in this case white to black. 

Because the animation-play-state is set to 'both', the transition remains however far along it got rather than resetting when your cursor moves off a pixel.


Since it's just HTML and CSS, you can customize your pixels using whatever CSS you fancy. Add intermediate color steps to the keyframes, adjust the animation-duration, change pixel size/shape, etc. Live it up!

