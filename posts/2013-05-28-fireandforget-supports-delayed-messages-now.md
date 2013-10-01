---
date: 2013-05-28 19:00
title: FireAndForget supports delayed messages now
author: Norbert Eder
tags: 
  - Message
  - Service
  - Bus
  - FireAndForget
  - .NET
  - delayed
  - bulk
template: post
---

[FireAndForget](http://devtyr.com/fireandforget.html "FindAndForget - Easy to configure, asynchronous message bus") is an easy to use and configure message bus. It is best used for tasks that are not time-critical. See the [original announcement](http://news.devtyr.com/post/fireandforget-easy-to-configure-asynchronous-message-bus "FireAndForget - Easy to configure, asynchronous message bus") for further information.

**Today**, version 0.2.0 has been released. The new version introduces the new feature **delayed messages**. Messages sent to FireAndForget can include a timestamp indicating an execution date/time. In fact, these messages are not executed immediately but rather at the time specified. 

In addition to this feature it is possible to mark delayed messages to be handled as a bulk message. In this case all delayed messages for a specified executor (an executor handles a message of a specific message type) are merged into one single message. This message will be executed by the given (bulk-enabled executor).

For further information, examples and a complete API documentation see [this page](http://devtyr.com/fireandforget.html "FireAndForget - Easy to configure, asynchronous message bus").

Feedback can be given via [@devtyr_com](https://twitter.com/devtyr_com "@devtyr_com") or the [G+ community](https://plus.google.com/u/0/communities/101936208491451882859 "DevTyr G+ community").
