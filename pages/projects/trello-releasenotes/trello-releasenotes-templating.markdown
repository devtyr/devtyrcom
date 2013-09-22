---
title: Templating
description: Generate release notes from Trello cards
author: DevTyr / Norbert Eder
category: trello-releasenotes
template: page_sidebar
---

## Templating

**trello-releasenotes** uses [Mu - a fast, streaming Node.js Mustache engine](https://github.com/raycmorgan/Mu) as the templating engine. Have a look at the [documentation](http://mustache.github.io/mustache.5.html) to get familiar with Mustache. A simple template (it's the default of trello-releasenotes):

	# {{header}} {{product}}
	{{version}} **{{version_number}}**

	{{generated}} **{{date}}**


	## {{subheader}}

	{{#data}}
	**{{name}}**
	{{#labels}}  `{{name}}` {{/labels}}

	{{#releasenotes}}
	> {{singleNote}}
	 

	{{/releasenotes}}
	{{/data}}
	{{^data}}
	No release notes available!
	{{/data}}

As you are able to configure the used templates within `settings.json` you can add new templates easily. Otherwise feel free to change the existing ones.

This is the available structure for templating:

	{
		"header": "",
		"product": "",
		"version": "",
		"version_number": "",
		"generated": "",
		"date": "",
		"subheader": "",
		"data": 
			[
				{
					"name": "",
					"labels": "",
					"link": "",
					"releasenotes": 
						[
							{ "singleNote": "" }
						]
				}
			]
	}

`data` is an array of all found cards. `releasenotes` is an array of all release notes found for the card.