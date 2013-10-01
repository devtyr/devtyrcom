---
date: 2013-02-14 20:00
title: Gullap - The static website generator (Mono)
author: Norbert Eder
tags: 
  - DevTyr
  - Gullap
  - static
  - website
  - generator
template: post
---

There are a lot of static website generators out there. Some of you might know [Jekyll](https://github.com/mojombo/jekyll "Jekyll"), based on Ruby. But there are just a handful solutions running on .NET/[Mono](http://www.mono-project.com "Mono"). One of them is [pretzel](https://github.com/Code52/pretzel "pretzel"). This project isn't maintained very well (last change about 10 months ago) and - in my opinion - to complex.

So I decided to create my own project, based on [Mono](http://www.mono-project.com "Mono"), [Nustache](https://github.com/jdiamond/Nustache "Nustache") (a [Mustache](http://mustache.github.com/ "Mustache") port) and [Markdown](http://daringfireball.net/projects/markdown/ "Markdown").

The project is in a really early stage and not available for the public at the moment. [DevTyr.com](http://devtyr.com "DevTyr.com") was created with an alpha version that works great for my needs. As soon as the project enters beta stage it will be published on [GitHub](https://github.com/devtyr/gullap "Gullap on GitHub"), as well as a solid documentation.

As an overview you can read about Gullap [here](http://devtyr.com/gullap.html "Gullap").

### Features of Gullap

* Based on [Mono](http://www.mono-project.org "Mono") it works on Windows and Linux
* Supports Markdown markup
* Supports Mustache templating engine
* Main menu is fully built based on the source files
	* Source file with Markdown markup are rendered as local HTML files
	* Source files can define external Links (no markup)
* Support for sidebar menus
* Include HTML to your markup files

### Feedback

If you are interested in the alpha version feel free to get in touch with me via [@devtyr_com](http://twitter.com/devtyr_com "@devtyr_com on Twitter") or the [G+ community](https://plus.google.com/u/0/communities/101936208491451882859 "DevTyr G+ community").