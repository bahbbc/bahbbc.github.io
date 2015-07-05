---
layout: post
title: Discovering Remark.js
subtitle: Presentations using Markdown, CSS and HTML
---

Almost didn't made it this week! It's been a crazy week with a lot of papers to write. But, here I am, and this time I'll talk about Remark.js. Last post was about LaTeX with an example of a presentation I made using it, and remark.js is another way to do presentations. (:warning: Attention! :warning: LaTeX is more than just for presentations)

![Could'n Sleep](/images/sleep.gif)

You probably already saw a presentation using remark once in your life if you see some presentation videos (like from Ruby Conf) with slides. They have a pretty simple layout and once again the objective is to keep the person is doing a presentation focus on the presentation content and then do some style to keep it good.

The creators made a [presentation](http://gnab.github.io/remark/#1) using the own remark to tell you what is it and why you should use it, but I'll summarize it for you:

 - Use markdown to make your presentations;
 - Use offline and display it in browsers;
 - Do a complete presentation in just one file;

The only thing you need is an HTML page. You can get an example in their [repo](https://github.com/gnab/remark) on github. And easy as that you already have one presentation! This file contains The CSS styling and the JS that imports the lib and makes the command to generate a new slideshow. But you can always keep things organized and separate a folder for the stylesheets and the javascripts.

So after this, I changed some font-style, importing new fonts from google. Added a backgound image for fun, using `background-image: url(image.jpg)` at the beggining of the slide and I already liked what I saw! (working with background images is a little tricky... Take care.)

Markdown gives you a lot of power to write a presentation and when you finish your styling is pretty simple finish the slides! Also, when you finish your css you can reuse it on your next presentations! :fireworks:

I just didn't get how to use emojis on it... I thought it would work as github flavored markdown and it didn't. (Maybe if I explore more I'll find out how to do it.)

This is the code for the first slide that I was using:

```
 class: center, middle

# Title

![Minion](http://i.giphy.com/1zzTnoZVsZqDK.gif)

```ruby
def add(a,b)
  a + b
```end

Notice how there is no return statement.
```
That generated this slide: (I just change the font to Pacífico on h1)

![Sample presentation](/images/slide_sample.png)

Embeding code is just like in github, but take care! Because if you have a style in the slide for center, the code will also be centered and will crash the indentation. :crying_cat_face:

I really liked it. :sparkling_heart: With a good font and background-color you can make a simple and beautiful presentation, and with markdown this is pretty easy. Looks pretty good for simple presentations and I'll start to use it instead of beamer in this cases. Beautiful presentations more handy!

<div style="text-align:center"><img src="/images/awesome.gif" width="300" height="170"></div>

If you want to know more about it check those liks:

- The github repo already mentioned above;
- The remark presentation also mentioned :stuck_out_tongue_closed_eyes:
- The [wiki](https://github.com/gnab/remark/wiki) (didn't mentioned that!)

Since I just made an introduction to remark, I'll try to make another post when I finished a slide using remark with a step-by-step tutorial, but If I can't, you already have a teste on how easy this is. :wink:
