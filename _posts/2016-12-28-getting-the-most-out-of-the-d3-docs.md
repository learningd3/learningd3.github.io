---
layout: post
title:  "Getting the Most out of the D3.js Documentation"
date:   2016-12-28
header-img: "reading-the-d3-docs.jpg"
image: /assets/img/posts/reading-the-d3-docs.jpg
description: "The D3 docs are one of the best ways to solve a problem you are encountering, or learn about areas in D3 that you were unaware of."
---

The D3 docs are one of the best ways to solve a problem you are encountering and learn about areas in D3 that you were unaware of. This post explains the basic conventions that are used in the D3 documentation. Let's look at three examples from the [API](https://github.com/d3/d3/blob/master/API.md).
<br>
<br>
<br>
d3.**selectAll**(*selector*)

In this example, the selectAll method is being explained.
Notice that the selectAll method is attached to the `d3` namespace. If the method being explained is not
attached to the `d3` namespace, the object it is attached to will be specified. The italicized word (`selector` in this case) is a description of the parameter
passed to the method.
<br>
<br>
<br>
selection.**property**(*name[, value]*)

While it might look like an array, parameters inside brackets (`value` in this case) signify an **optional** parameter. The comma included inside the bracket reinforces that idea.
<br>
<br>
<br>
d3.**csv**(*url[[, row], callback]*)

Here we have a required parameter `url` and two optional parameters `accessor` and `callback`. In this case, if you provide two parameters to the `.csv` method, they will be the url and the callback. However, if you provide 3 parameters, the second will be the accessor parameter, not the callback parameter.
<br>
<br>
### Understand what's actually happening
You will inevitable get stuck as you get better at D3
Get into the habit of going to the docs first.
Make sure you understand the purpose of the methods you trying to use.
You might be surprised to find that these methods are more powerful then you expected.

If you're interested in learning more about D3, I made something for you.
It's a comprehensive and concise course for learning the D3.js library.
You can learn more about it [here](https://learningd3.com), or sign up for a free lesson below.
