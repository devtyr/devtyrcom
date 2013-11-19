---
date: 2013-11-19 20:00
title: Generate RSS Feed with Gullap
author: Norbert Eder
tags: 
  - Gullap
  - static
  - website
  - generator
  - RSS
  - feed
template: post
---

Version 1.3.0 of `Gullap` is under heavy development. One of the new features supports the customization of the target file name for posts as well as for pages. In the prior versions everything was generated into files having an HTML extension.

This change makes it easy to generate everything you might want to generate. This post shows an example of a Mustache template to generate a simple RSS Feed.

	<?xml version="1.0" encoding="UTF-8"?>
	<rss version="2.0" xmlns:atom="http://www.w3.org/2005/Atom">
	<channel>
	        <atom:link href="http://devtyr.com/rss.xml" rel="self" type="application/rss+xml" />
	        <title>{{site.config.title}}</title>
	        <generator>Gullap 1.2.0.0 - http://devtyr.com/gullap/</generator>
	        <description>DevTyr News Feed</description>
	        <link>http://devtyr.com</link>
	        <language>en-US</language>
	        <lastBuildDate>{{site.time}}</lastBuildDate>
	        <webMaster>office@devtyr.com (DevTyr Webmaster)</webMaster>
	        {{#site.posts}}
	    <item>
	            <title>{{title}}</title>
	            <link>http://devtyr.com{{url}}</link>
	            <author>{{author}}</author>
	            <description><![CDATA[{{{content}}}]]></description>
	            <pubDate>{{date}}</pubDate>
	            <guid>http://devtyr.com{{url}}</guid>
	    </item>
	    {{/site.posts}}
	</channel>

Save this to `rss.template` as it will be referenced by a page we need to create too:

	---
	title: DevTyr RSS
	description: DevTyr RSS Feed
	author: DevTyr / Norbert Eder
	template: rss
	filename: rss.xml
	---

See the new attribte `filename` within the YAML Front Matter. Use it to define a new filename which will be recognized by the generation. 

> Please note: If you override the filename, you have to set the extension as well. Defining `my-new-page` will NOT result in a generated file named `my-new-page.html`.

After creation of both files generate the whole site or just the file and have a look your working RSS feed.