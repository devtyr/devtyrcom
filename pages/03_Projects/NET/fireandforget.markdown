Title: FireAndForget - DevTyr
Description: Easy to configure, lightweight and asynchronous message bus
Keywords: FireAndForget, Message, Service, Bus, Lightweight, Asynchronous
Author: DevTyr / Norbert Eder
Menu: Projects
MenuTitle: FireAndForget
MenuCategory: NET
Sidebar: FireAndForget
SidebarTitle: About
Template: page_sidebar
Directory: projects/fireandforget
-----

## About

*FireAndForget* is an easy to configure, lightweight, asynchronous *message bus* coming with a very low set of dependencies. It is based on Microsoft *.NET Framework 4.5*. The message bus can be accessed via JSON REST API.

The main goal of this project is to provide a message/service bus that handles messages without the need of a callback to the main application ("fire and forget"), although it might be implemented by a custom executor. As all communication is done via a JSON REST API FireAndForget runs out of process and helps saving ressources for non time critical but performance intensive tasks.

There are a lot of Enterprise Service Bus (ESB) implementations but all of are very complex. This includes configuration, implementation and maintenance. They are great if you have a range of wide scenarios to handle but they are oversized for simple tasks you want to run out of process (e.g. notifications, ...). This is why FireAndForget saw the light of day.

### Feedback

Please help to improve FireAndForget by giving feedback. This can be done via [@devtyr_com](https://twitter.com/devtyr_com "@devtyr_com") or the [G+ community](https://plus.google.com/u/0/communities/101936208491451882859 "DevTyr G+ community").
