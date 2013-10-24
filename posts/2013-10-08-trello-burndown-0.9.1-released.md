---
date: 2013-10-08 11:00
title: trello-burndown 0.9.1 released
author: Norbert Eder
tags: 
  - Trello
  - burndown
  - chart
  - scrum
  - node
template: post
---

`trello-burndown 0.9.1` is available now. The following features and fixes are included:

* Support for Scrum for Trello Chrome extension
* Fix when a card in one of the columns doesn't have a correct match syntax and hence as a result caused the server to crash [Juri Strumpflohner](https://github.com/juristr "Juri Strumpflohner")
* Adding console.log to write out the card that failed the regex check [Juri Strumpflohner](https://github.com/juristr "Juri Strumpflohner")
* Fix to also fetch cards of finished lists
* Graph `done estimate` shows progress up to current date
* Added optional parameter `boardId` to CLI

You can download this version via [GitHub](https://github.com/devtyr/trello-burndown/releases/tag/v0.9.1 "trello-burndown 0.9.1 on GitHub") or as [NPM package](https://npmjs.org/package/trello-burndown "trello-burndown NPM package").

If you want to get in touch with me, see the [contact page](http://devtyr.com/contact.html "DevTyr Contact"). 