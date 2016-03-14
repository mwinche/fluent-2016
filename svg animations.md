SVG Animations
==============

## Sarah Drasner @sarah_edo, Zillow

[Slides](http://slides.com/sdrasner/fluent-keynote#/)

Animations command attention.

SVG is crisp on any display. Less HTTP requests. Easily scalable and small filesize.
Easy to animate. They have a DOM that you can animate. Accessible, and fun!

SVG has incredible support (especially post IE8). Need a GUI to optimize your SVG (SVGO/SVGO-GUI, SVGMG).

SVG Sprites. Can use for responsive. A responsive, beautiful SVG example as 8KB gZipped.

CSS animation (using negative delay).

Animation media queries. Use CSS for width and height. No width/height in SVG itself.

Define a ViewBox and move it with JavaScript (coming spec so you can do in CSS).

GSAP is the tool she's using to animate in JS:
* DrawSVG
* MorphSVG
* CSS Props
* Draggable
* Motion along a path
* timeline
* relative color tweening
* CycleStagger
* solves cross browser inconsistencies
