---
layout: post
title: Spicing Sublime!
---

It's been a while... Sorry about that. Too many work to do :pensive:... I'll try to do two posts this week to compensate. (since I broke my promise) They will be quick posts (with some of information I gathered those weeks)

<div style="text-align:center"><img src="/images/guilty_dog.gif" width="300" height="170"></div>

Last week (actually, it's been two weeks, I guess) I was reading a [post](http://devblog.avdi.org/2015/07/08/ruby-is-defined-by-terrible-tools/) from Avdi Grimm about ruby beeing defined by terrible tools.
I won't discuss the blog post, but it made me think on how much I suffer using only sublime to program. I installed RubyMine (academic license), but I have some agility with Sublime and maybe I like to suffer, so I am having some trouble to change.
The think is: I started to improove my Sublime. For those who aren't familiar, [Sublime](http://www.sublimetext.com/) is a text editor for code. There are lovers and haters and I still like it.

So, you can improve Sublime installing packages on it. The first thing to do is install [Package Controll](https://packagecontrol.io/installation). Is pretty simple and easy. I already used [All Autocomplete](https://packagecontrol.io/packages/All%20Autocomplete), [GitGutter](https://packagecontrol.io/packages/GitGutter) and the [Rails Casts Colour](https://packagecontrol.io/packages/RailsCasts%20Colour%20Scheme).
I also use a nice settings config to help me. And then, I read Avdi Grimm's post and those things didn't seen enough. I wanted to add something to prevent me to add inconsistent style to the code. Something that helps me findind that damn wrong comma that is broking everything. I wanted rubocop on Sublime.

<div style="text-align:center"><img src="/images/police.gif" width="300" height="170"></div>

[Rubocop](https://github.com/bbatsov/rubocop) is a gem that analyses your code according to the community [Ruby Style Guide](https://github.com/bbatsov/ruby-style-guide). After installation you can run it in your command line and voilà! It will show all the 'Offenses' you have commited.
He is pretty annoying. If you are used to program like there is no tomorrow, he will stop you (or, at least piss you off pointing your offenses). It's easy to configure a new yml file that changes it's normal behaviour (at least is what the documentation says).

I didn't want to keep running this at the console. It could be nice to do it together with RSpec, but no, thanks. So, I discovered [Sublime Linter](https://packagecontrol.io/packages/SublimeLinter). I didn't knew what the world 'linter' was.
According to wikipédia:

> In computer programming, lint was the name originally given to a particular program that flagged some suspicious and non-portable constructs (likely to be bugs) in C language source code.
> The term is now applied generically to tools that flag suspicious usage in software written in any computer language. The term lint-like behavior is sometimes applied to the process of flagging suspicious language usage.
> Lint-like tools generally perform static analysis of source code.

Just what I wanted :relaxed: but, it does not work alone. From the docs:

> SublimeLinter does not do the linting itself; it acts as a host for linting plugins.
> The linting plugins themselves usually do not perform linting either; they just act as a bridge between the code you type in Sublime Text and the actual linter.

It supports many languanges, you can install as much linting plugins as you want! Take a look on what they say about using a linter:

"Programming is hard. We are bound to make mistakes. The big advantage of using SublimeLinter is that your code can be linted as you type (before saving your changes) and any errors are highlighted immediately, which is considerably easier than saving the file, switching to a terminal, running a linter, reading through a list of errors, then switching back to Sublime Text to locate the errors!"

<div style="text-align:center"><img src="/images/omg.gif" width="300" height="170"></div>

If you use eclipse you are judding me now... I know... But I don't care.(that's one thing the post metions. Don't be lazy and read it.)

Now let's add [SublimeLinter-ruby](https://packagecontrol.io/packages/SublimeLinter-ruby) and [SublimeLinter-rubocop](https://packagecontrol.io/packages/SublimeLinter-rubocop) to see the magic happening. You will just need to configure the ruby path in Preferences -> Package Settings -> Sublime Linter -> Settings - Default.
This is my example:

```
"paths": {
            "linux": ["~/.rvm/rubies/ruby-2.1.3/bin/ruby"],
            "osx": [],
            "windows": []
        },
```

Also you will need to install the rubocop gem. You can install in the folder that all your projects are.Now, get ready to see some 'offenses' in yellow and when you broke anything in red. The bad thing is that I couldn't make the personalized .yml work when I installed the gem in my workspace folder. :expressionless:
When I did, I'll edit this post.

![Image of rubocop offenses](/images/rubocop-linter.png)


