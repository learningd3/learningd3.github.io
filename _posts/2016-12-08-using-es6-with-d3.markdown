---
layout: post
title:  "Using ES6 with D3.js"
date:   2016-12-6
---

ES6 is the next version of Javascript, and it has some great features that you can start using with your D3.js visualizations.

## Getting set up
If your project doesn't use ES6 already, you'll have to set up your project to use it. You can use [https://babeljs.io](Babel) to compile your ES6 ready JavaScript to JavaScript that works in all the browsers.

You can check out instructions on how to get it set up here.
I recommend using the [https://babeljs.io/docs/usage/cli/](cli tool) if you are comfortable with the terminal.


## Arrow Functions
{% highlight javascript %}
.attr("y", d => d.y)
.attr("x", (d, i) => i * 10)
{% endhighlight %}

Arrow Functions provide a shorter syntax for writing anonymous functions in JavaScript. If you have one argument you don't need to include parenthesis. If you you have 0 or 2+ arguments you need to include arguments. You can use these all over your d3 code to replace anonymous functions you use as a second parameter to the `.attr()` methods and in lots of other places. Anytime you normally write an anonymous function, you can replace them with the arrow function.

## Let and const
{% highlight javascript %}
let x = 10;
const y = 20;
{% endhighlight %}

Instead of using var for your variables you can be more explicit about the type of variable you want. `let` works the same as `var` but it's block scoped, so if you use it inside an if statement, it won't spill out. `const` is like `let` but it once it has been assigned a value it won't let you reassign a value.

## Import
{% highlight javascript %}
import * as scale from "d3-scale"
{% endhighlight %}

One of the nice things about d3.v4.js is that it is broken up into modules. You can import modules into your js files in a way that makes more sense. Because D3 modules don't export a default object, you'll need to use this star syntax.

## Destructuring Objects
{% highlight javascript %}
const { blue } = colors;
{% endhighlight %}

Destructuring an object is where you take out key value pairs from an object, assigning the name of the key to your variable, and the value, to the value of the variable. In this example i'm creating a constant named blue, that is assigned to whatever `colors.blue` is.

## Method Shorthand
{% highlight javascript %}
{
  sayHello() {
    return "Hello!"
  }
}
{% endhighlight %}

You can abbreviate methods. Instead of writing an anonymous function that's assigned to a key, you can put parenthesis and a block statement.

## Template Strings
{% highlight javascript %}
.attr("transform", `translate(${x}, ${y})`);
{% endhighlight %}

You can insert javascript variables and expressions into strings with this handy syntax. First, make sure you use the back tick instead of the single or double quote. Whenever you just need to put a dollar sign with brackets surrounding the variable or expression. These strings can also be multi line!

## Default Parameters
{% highlight javascript %}
function(data = "n/a") { }
{% endhighlight %}

You can set a function parameters default value by adding an equal sign and then the value you want as the default. If the function is called without the parameter, or with a parameter set to `undefined` the default value will be assigned.


There's a more to ES6 than what I showed here but if you're looking to get your feet wet, give these examples a try. Once you start adopting the syntax, it's hard to go back!

If you like this post, you should check out my full course on D3. You can read more about it below and sign up for a free lesson!
