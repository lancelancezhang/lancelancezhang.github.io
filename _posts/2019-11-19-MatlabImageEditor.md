---
layout: splash
title: "Action Shot and Remove Action"
date: 2019-11-19
tags: [image editing, matlab]
author_profile: false
header:
excerpt: "Editing images to Action Shots and Removing Actions using MatLab"
---

## Project Outline

This action shot and remove action was my project as part of my first year engineering programming paper ENGGEN 131.

An example of its functions can be seen in the images below with the following set of 4 images:

<img src="{{ site.url }}{{ site.baseurl }}/images/matlab/Overview.JPG" alt="">


Action Shot

The action shot function that I wrote combines each of the images in the set to create an 'action shot':

<img src="{{ site.url }}{{ site.baseurl }}/images/matlab/Action Shot.JPG" alt="">


Remove Action

The image remover script on the other hand does the opposite - it uses the three images in order to remove objects from the images to create 'remove action' image:

<img src="{{ site.url }}{{ site.baseurl }}/images/matlab/Remove Action.JPG" alt="">

Another example of the action shot and the remove action being applied is also seen in the example below:

Images Overview

<img src="{{ site.url }}{{ site.baseurl }}/images/matlab/Overview 2.JPG" alt="">

Remove Action

<img src="{{ site.url }}{{ site.baseurl }}/images/matlab/Remove Action 2.JPG" alt="">

Action Shot

<img src="{{ site.url }}{{ site.baseurl }}/images/matlab/Action Shot2.JPG" alt="">


The biggest challenge I faced creating this code was the initial visualisation of
how the rgb layers interacted with one another in order to form a whole image, and
being able to use the correct syntax and brackets/braces to enter specific pieces
of information in what were esentially 4D arrays.
