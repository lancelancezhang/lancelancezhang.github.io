---
layout: splash
title: "Space Shapes"
date: 2020-5-23
author_profile: false
tags: [java, OOP, GUI, Graphics]
header:
excerpt: "Space Shapes Assignments"
---
# Space Shapes Assignment

{% include video id="1TB_uMgRHLYvgC_je-RoiJOOxwuUReDUM" provider="google-drive" %}

This assignment was based around implementing shapes into a graphical user interface
that would bounce around the screen like the DVD logo would when on pause on a TV.

Specifically, I was tasked with developing different shapes that were child classes
of the Shape parent hierarchy. These shapes included, ovals, hexagons, dynamic shapes
and carrier shapes.

### Dynamic Shapes
The special property of the dynamic shape was that it would change its colour when
hitting the side of the wall and revert back when hitting the top or bottom.

This property can be seen below:

<img src="{{ site.url }}{{ site.baseurl }}/images/spaceshapes/shape2.JPG" alt="">


### Carrier Shapes
The implementation of this shape was probably the most tedious and difficult of the
entire assignment. The property of a carrier shape was that it would be the parent
class of child classes when other shapes were added into it. This meant that the carrier
shape was capable of carrying smaller shapes inside of it, including carrier shapes
themselves, which would bounce around based on the new bounding box.

It was most difficult to get understand and figure out the coordinates that each
carrier shape needed to be adjusted in order to get the correct boundaries.

An example of this can be seen below:

<img src="{{ site.url }}{{ site.baseurl }}/images/spaceshapes/shape1.JPG" alt="">


Despite the difficulty of the assignment task, the most important aspect of it was
that the program was crafted under good Object Oriented Programming practice, with
good design. This meant that my code went through several iterations where repeated
code was deleted, moved and adjusted, with me attempting to find a balance between
code that functioned as intended, but also designed well.

The end result, unlike other assignments that I had completed was a satisfying
graphical user interface where all the shapes correctly interacted with one another.
