---
layout: post
title:  "Creating Generative Art with D3.js"
date:   2016-12-28
header-img: "reading-the-d3-docs.jpg"
image: /assets/img/posts/reading-the-d3-docs.jpg
description: "The D3 docs are one of the best ways to solve a problem you are encountering, or learn about areas in D3 that you were unaware of."
---

I took a trio to the SFMoma recently where I came across the work of Sol LeWitt. One of the interesting things about Sol's work was that he created the rules of his art pieces, but they were executable by anyone. I wanted to see if anyone had recreated Sol's pieces using D3.js. When I did a quick search I found that Chuck Grimmet had made some pieces which was really inspiring.

It got me interested in the idea of generative art.

## Recreating an art piece, in code.
I created this heart using illustrator around 8 years ago. It took me forever. I wanted to see how difficult it would be to create something similar using D3.js. I wanted a technique that allowed me to create a similar effect using any SVG path.

First, I create a grid of SVG circles, and colored them using a scale from color brewer.
[IMG]

Next, I imported a SVG path and tried to detect whether the center of a circle was inside the path. There's a way to detect this in d3 for polygons, but I wasn't able to find a solution for paths. Thankfully, I found a canvas method called isPointInPath that allowed me to do what I wanted.

[IMG]

This effect was really great on its own. But it's not what I wanted for this piece. I didn't want a grid based distribution. I wanted it to look like a human placed the circles, which i why I decided to use an alorithm.

I was really inspired by Mike Bostock's example of Mitchell's best candidate. What this algorithm does takes a number of candidates. Plots them randomly, and then chooses the best candidate based on whatever point is farthest from all the others.

Using this algorithm, I was able to get my final result.


I'm happy with it, but there are two problems I would love to have solved.

The first being the ability to detect whether or not a point is inside a path using SVG. Canvas is fine, but there are certain things I'd like to do with animations that are harder using canvas.

The second thing would be the ability to prevent circles from escaping the bounds of the path. Right now, i'm only checking the center of the circle to make sure it stays within the path.  There's probably a way to detect that the perimeter of the path hasn't escaped but I haven't found it yet.


## Some Inspiration
If you've generated art with with code, or know of anyone who has, i'd love to see it. Below are some people that i've been following that have made beautiful pieces of art.

1. Anders Hoff
2. Kristen Henry
3. Dan Eden
