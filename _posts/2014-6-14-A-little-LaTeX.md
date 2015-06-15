---
layout: post
title: A little about LaTeX
---

Since I started working with research, the teachears loved to talk about LaTeX and how it can help us save time writting our papers.
How it's beautiful and how you can do lots of stuff easily that you can't with Microsoft Word. (Let's not talk about open office, it wouldn't be a fair fight)

So, if you don't have any ideia what *LaTeX* is, you already have a clue. It's something to write texts. Take a look on what they say on (latex-projext)[http://www.latex-project.org/] "LaTeX is a high-quality typesetting system; it includes features designed for the production of technical and scientific documentation that runs on top of Donald E. Knuth's TeX typesetting system"

Different from Libre Office that is a WYSWYG (What You See is What You Get), with LaTeX you will write your text and formating configuration in one file, and you don't have to worry with the design of the document (unless you want to create your own, but let's talk about it later) and just worry about what you're going to talk about! The output format normally is a pdf, what is cool because pdf works everywhere. This code below shows a presentation, it's really easy to understand.

```tex
\documentclass{beamer}
\title[My title]{SOLID}
\author{Bárbara Barbosa - @bahbbc}
\institute{BankFacil - @BankFacilDev}
\date{\today}

\begin{document}

\begin{frame}
  \titlepage
\end{frame}
```

The first line says that this document class is beamer... This means that this doc is actually a presentation. Normaly docs would have a class like `\documentclass{article}` or something else. Beamer is a pesudo-anglicism for video projector (I didn't know that :grin:). So you can say that this is a presentation about SOLID, the author is myself, it was presented at BankFacil in... Today? What? Well, this is a helper that keeps the date when the file is compiled. With this, the date will keep changes until you finish working on it. Not very good if you procrastinate too much to finish your docs. :wink:

So, now I'll start the presentation. Every slide is a frame and I can write all my text on each. The magic inside Latex is that you can use a theme and don't worry about the design configs anymore :heart: You can also make your own theme and never worry about designing it again! It isn't beautiful? :heart:
Some other lovely things you can achieve using LaTex:
  - Put figures wherever you like;
  - Formulas (oh, the formulas!) will never move, are easy to make and will always be like inside a Calculus book;
  - Your summary will always be right;
  - Text format changes can be made for the whole document with just a few commands;
  - Your sections, figures, tables, citations... will be automaticaly numbered.

This is really good when you want to submit a paper to a conference that has the LaTeX format. You just have to worry about your text and how you will make you 6-months work fit in 10 pages. :laughing: You won't have to worry about adjusting your file into theirs rules.

<div style="text-align:center"><img src="/images/type_crazy.gif" width="300" height="170"></div>

When after formating everything you have 11 pages, and the conference only accept max. 10 pages papers :fearful:

---

LaTex is a free software and it works on Linux, Mac OS and Windows :stuck_out_tongue:. When I used LaTeX offline I liked the MiKTeX distribution (http://miktex.org/). It comes with a graphic interface called TeXworks. This only works for windows (I hadn't met the light yet at that time)

<div style="text-align:center"><img src="/images/ruindows.gif" width="300" height="200"></div>

But today I like to use [Overleaf](https://www.overleaf.com/).

![Image Overleaf Dash](/images/dashboard.png)

Overleaf it's pretty straitforward, you make your registration and have 100MB free to make your files. You will have you dashboard and a lot of themes to work on your docs. You can also upload your own theme. The coolest think is that the file keeps compiling while you are writing and shows the result in your right. When you write some shit you are immediately notified.

![Image Overleaf Screen](/images/2-screens.png)

Also you can work together with your co-workers! Is not as good as google docs it is. The texts keeps moving and you don't know what is happening. There is no sign that other people are editing the file, but I never had a problem with it. You can also leave comments to you friend (comments in LaTeX are `%`) and he will see it right away :relaxed:

Take a look at the [SOLID presentation](http://www.slideshare.net/bankfacil/solid-ood-principles) I made using Overleaf.

So if I was able to pass some of my LaTeX love to you and you're curious about it check those links:

 - [The Not So Short Introduction To LaTeX](http://linorg.usp.br/CTAN/info/lshort/english/lshort.pdf)
 - [Introdução ao LaTeX -- pt-br](http://www.mat.ufmg.br/~regi/topicos/intlat.pdf)
 - You can also learn a lot using Overleaf as an editor and chacking out the code that it shows.

  Now just start making your beautiful files.

<div style="text-align:center"><img src="/images/minions_happy.gif" width="500" height="270"></div>

Ps. Besides Steam Summer sale, I made it! :star2:
