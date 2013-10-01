---
date: 2013-04-26 14:30
title: trello-burndown 0.9.0 released
author: Norbert Eder
tags: 
  - Node
  - NPM
  - Trello
  - burndown
  - sprint
  - scrum
template: post
---

[trello-burndown](http://devtyr.github.io/trello-burndown/ "trello-burndown") 0.9.0 is ready for download. There were several problems running trello-burndown with node.js 0.10.x. These problems where caused by the module `restler` which is used by the module `trello`. As I wrote [here](http://news.devtyr.com/post/trelloex-0.1.0-released "trello_ex 0.1.0 released") I forked the module and did some changes. The new module has been integrated into trello-burndown. Now it works with 0.10.x as expected.

## Changes

* Removed dependencies to trello and restler due to incompatibility with node 0.10.x
* Added dependency to trello_ex
* Minor refactorings

You can get trello-burndown via [npm](https://npmjs.org/package/trello-burndown "trello-burndown on npm"). To use the latest bits, have a look at [GitHub](https://github.com/devtyr/trello-burndown "trello-burndown on GitHub"). If there are some issues, please [let me know](https://github.com/devtyr/trello-burndown/issues "trello-burndown issues").

Feedback can be given via [@devtyr_com](http://twitter.com/devtyr_com "@devtyr_com") or the [G+ community](https://plus.google.com/u/0/communities/101936208491451882859 "DevTyr G+ community").
