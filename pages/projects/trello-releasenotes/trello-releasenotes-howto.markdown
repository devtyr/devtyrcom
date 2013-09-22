---
title: How To
description: Generate release notes from Trello cards
author: DevTyr / Norbert Eder
category: trello-releasenotes
template: page_sidebar
---

## How To

### Export

To export release notes start it like shown bellow:

	node index.js -g [LISTNAME(S)]

Replace `[LISTNAME(S)]` with the name of your list that contains the cards and release note for export. In this case the configured `boardId` from `settings.json` will be used to find the internal id of `[LISTNAME(S)]`. In case you have different boards, you can override the configured `boardId` by using the `-b` option.

	node index.js -g [LISTNAME(S)] -b [BOARDID]

If you want to run a job updating your release notes it might be helpful to set the version by an parameter. This can be done by using the parameter `-v`.

	node index.js -g [LISTNAME(S)] -b [BOARDID] -v [VERSION]

### Example

To export all release notes of list 'Done' execute

	node index.js -g Done

It is also possible to export release notes of several lists. Call it like this:

	node index.js -g "My List 1, My List 2"

This will search `My List 1` and `My List 2` for cards having release notes.


Please note that the result is a `.markdown` file that can be processed with other modules like [ideamark](https://github.com/devtyr/ideamark "ideamark") or [mdserv](https://github.com/Bonuspunkt/mdserv "mdserv"). In this combination you can directly serve your exported release notes via HTTP.

### Which cards will be exported?

All cards of the given list having comments that start with `RELEASE:` (default) are exported. If there are multiple entries having this "flag", all of them are exported. You are able to change this setting in `settings.json`, change `releaseIdentifier` to a value you like to use.

> Please note that all lists (also archived ones) are considered.

### Show available lists

In some cases it is very helpful to view the lists available within the configured board. To get an overview use the option `-l` or `--list`:

	node index.js -l

This will come up with a complete list, showing the status (open, closed), list id and the name. It's also possible to get a list of a specific status. This options are available:

	node index.js -l all       The same as -l without a parameter
	node index.js -l open      Shows all lists that are not archived.
	node index.js -l closed    Shows all archieved lists

## Usage from other modules

It is also possible to use this module from another one. For example to receive all cards having release notes for the specified lists:

	var TrelloReceiver = require('./lib/cardreceiver.js');

	var lists = ["list1", "list2"];
	var receiver = new TrelloReceiver("applicationKey", "userToken", "boardId");

	receiver.receive(lists, function(err, cards) {
		if (err) {
			// handle error
		}

		// do something with your cards here
	});

It's also possible to work with lists:

	receiver.getLists(filter, function(error,data) {
		if (error) {
			console.log(error instanceof Error ? error.message : error);
		} else {
			if (data) {
				for (var i = 0; i < data.length; i++) {
					console.log((data[i].closed ? '[closed] ' : '[open]   ') + data[i].id + ' ' + data[i].name);
				}
			}
			
		}
	});

The filter defines (if set) which lists to be received. Possible values based on the Trello API:

- none
- open
- closed
- all