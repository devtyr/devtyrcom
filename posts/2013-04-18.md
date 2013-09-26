---
date: 2013-04-18 12:30
title: trello-burndown 0.8.0 available
author: Norbert Eder
tags: 
  - Trello
  - burndown
  - sprint
  - node
template: post
---

Version 0.8 of [trello-burndown](http://devtyr.github.io/trello-burndown/ "trello-burndown") is available for installation via [NPM](https://npmjs.org/package/trello-burndown "trello-burndown on NPM").

## Release notes

See the release notes below.

### Bugs

* Sprint was disabled one day to early
* 'export' and 'config' folders are created on startup now if they don't exist
* Removed d3.js as a NPM module due to incompatibility with node 0.10.x; added as a static resource
* Work done on none work days won't be tracked
* Changed sprint burndown for uniformity

### Features

* Mouseover for data points
* Support of multiple finished lists
* Unfinished tasks are shown on current sprint (web)
* Statistical data on current sprint

Feedback can be given via [@devtyr_com](http://twitter.com/devtyr_com "@devtyr_com") or the [G+ community](https://plus.google.com/u/0/communities/101936208491451882859 "DevTyr G+ community").
