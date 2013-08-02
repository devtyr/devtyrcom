Title: Trello Release Notes - Installation - DevTyr
Description: Generate release notes from Trello cards
Author: DevTyr / Norbert Eder
Menu: trello-releasenotes
MenuTitle: Installation
Sidebar: trello-releasenotes
Template: page_sidebar
Directory: projects/trello-releasenotes
-----

## Installation

You can install it using `npm`.

	npm install trello-releasenotes

### Obtain a Trello token

First, log in to Trello and open [Generate API Keys](https://trello.com/1/appKey/generate "Generate API Keys"). You'll receive an key to use in the next step.

Second, call https://trello.com/1/authorize?key=YOUR_KEY&name=trello-releasenotes&expiration=never&response_type=token to grant access for this application. Be sure to replace `YOUR_KEY` with the key received in the first step.

> For further information visit: [Getting a Token from a User](https://trello.com/docs/gettingstarted/index.html#getting-a-token-from-a-user "Getting a Token from a User")

Store the key from the first action in setting `applicationKey` of `settings.json` and the token received from the second step in `userToken`.


## Usage

There are some settings you can set up in `settings.json`:

	applicationKey		Insert your obtained application key from Trello to get access to it
	userToken			Define your user token you'll receive when obtaining an application ey
	boardId				Define the id of the board you want to search for release notes
	releaseIdentifier   Default is set to 'RELEASE:'
	template			Defines the template to use
	exportLinks			if true, links are written to the exported data; the default template is able to handle that
	exportPath			Set a path if release notes should be exported to a specific path
	titleReplacePattern A replace regular expression to replace parts of the title (export)
	strings				These are used to create the export, translate them into your language if you want

> `version` and `product` of `strings` are used to generate the filename. 

### How to obtain the board id

When you open your Trello account you get a list of boards, open one of it and the URL will be something like

	https://trello.com/board/boardname/identifier

Copy `identifier` and set this one as the `boardId` in `settings.json`. This is used to search for lists if there is no command line option that overrides that setting.
