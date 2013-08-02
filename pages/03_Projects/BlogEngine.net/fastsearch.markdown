Title: FastSearch - DevTyr
Description: Ajax Search for BlogEngine.NET 
Author: DevTyr / Norbert Eder
Menu: Projects
MenuTitle: FastSearch
MenuCategory: BlogEngine.NET
Sidebar: FastSearch
SidebarTitle: Features
Template: page_sidebar
Directory: projects/fastsearch
-----

## Features

* FastSearch control
* SearchService
* FastSearch page to link from your webpage
* Widget
* Single search box

FastSearch provides an AJAX search for your BlogEngine.NET based website.

FastSearch can be seen as a replacement of the existing BlogEngine.NET search functionality. It can be used as a specific search page, as a search widget or just a search page. All applied styles can be overwritten in your theme's stylesheet.

> **Please note**: FastSearch uses the existing search functionality of BlogEninge.NET (for insiders: Search.cs).

FastSearch was developed for BlogEngine.NET 2.5. It was not tested with lower versions.

## Dependencies

FastSearch uses [jQuery](http://jquery.com/ "jQuery") (which is already used by BlogEngine.NET) and [Knockout.js](http://knockoutjs.com/ "Knockout.js"). Knockout.js is included in the package (version 2.0.0).

## Installation

Extract all contents to the root of your web application. After that you can link to FastSearch.aspx from your menu. The widget is available within the widget-list. To use this search as a single search box you have to include the control into your site.master:

	<%@ Register Src="~/User controls/FastSearch.ascx" TagName="FastSearch" TagPrefix="fs" %>
	<fs:FastSearch id="fastsearchcontrol" ShowSearchFieldOnly="true" runat="server" />

If you use it as a single search box, set the property `ShowSearchFieldOnly` to `true`.

## Thanks

Kudos to [@klaus_b0](https://twitter.com/klaus_b0 "@klaus_b0"), [@Anheledir](https://twitter.com/Anheledir "@Anheledir") and [@michaelhorkavy](https://twitter.com/michaelhorkavy "@michaelhorkavy") for testing and supporting!
