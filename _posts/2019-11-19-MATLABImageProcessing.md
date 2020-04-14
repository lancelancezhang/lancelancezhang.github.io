---
layout: splash
title: "MATLAB Image Processing"
date: 2019-11-19
tags: [image editing, MATLAB]
author_profile: false
header:
excerpt: "Processing Action Shot and Remove Action functions in MATLAB"
---
# MATLAB Image Processor

This my final MATLAB project that I did for a programming paper.

The project was the implementation of a photo processing program that dynamically
edited 4D arrays inside of MATLAB in order to remove or add elements into the
layers. This could be done through input of a set of images or from a video.


An example of its functions can be seen in the images below with the following set of 4 images:

<img src="{{ site.url }}{{ site.baseurl }}/images/matlab/Overview.JPG" alt="">


**Action Shot**

The action shot function that I wrote combines each of the images in the set to create an 'action shot':

<img src="{{ site.url }}{{ site.baseurl }}/images/matlab/Action Shot.JPG" alt="">


**Remove Action**

The image remover script on the other hand does the opposite - it uses the three images in order to remove objects from the images to create 'remove action' image:

<img src="{{ site.url }}{{ site.baseurl }}/images/matlab/Remove Action.JPG" alt="">

Another example of the action shot and the remove action being applied is also seen in the example below:

**Images Overview**

<img src="{{ site.url }}{{ site.baseurl }}/images/matlab/Overview 2.JPG" alt="">

**Remove Action**

<img src="{{ site.url }}{{ site.baseurl }}/images/matlab/Remove Action 2.JPG" alt="">

**Action Shot**

<img src="{{ site.url }}{{ site.baseurl }}/images/matlab/Action Shot2.JPG" alt="">


The biggest challenged faced in this implementation was the initial visualisation of how the RGB
layers interacted with one another in order to form a whole image. Once this was figured out, it
was just figuring out correct syntax, brackets/braces needed to enter specific layers of each images
so that the image processing could take place.

This project was really rewarding to do and gave insight into how a lot of modern image processing in
some applications like photoshop actually function - things we don't typically think about when we use them so freely.
