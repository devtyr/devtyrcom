---
title: History
description: Hours Tracker for Windows Phone is a mobile app to track work hours for projects
tags: 
  - time tracking
  - time record
  - windows phone
  - time
  - tool
  - working
  - hours
  - tracker
author: DevTyr / Norbert Eder
category: Working Hours Tracker
template: page_sidebar
---

## History

### 1.9.0.0

One of the major features coming with this version is the `SkyDrive` integration. This feature was the most requested one - and here is it!

#### Improvements and features

* `SkyDrive` integration (export and backup)
* Show tracking time on app's start screen
* Added `Customer` information to project and all project selections
* Updated layout of project details
* Empty list information for project summary if no data has been entered
* Show default billing rates in activity list
* More spacing between associated activities in project detail view
* Improved icons for start screen

#### Bugfixes

* English news tile translation

### 1.8.0.0

There is a great response for this app and a lot of ideas and improvments are sent every day. This version considered a lot of usability issues and resolved them.

#### Improvements

* Better performance. There was a lot of feedback that the app is getting slow when having more and more time records. This should be better now, as not everything is loaded everytime, just when it's needed. Furthermore there won't be a reload when no records have changed or added.
* Renamed `export` into `backup`. This was a misleading translation as this main menu item makes a backup of the databases (in case you have to restore it someday). There is also some more help text to let the user know where to find the export functionality.
* The `monthly list` got a new design. There was a lot of feedback to show the description permanently. Additionally also the activity of the record (if set) will be shown now. The break time has been removed, as this should be less important. The list itself should also be faster now.
* While logging on to Dropbox the page title hides now. Some of you reported that it is not possible to login to Dropbox. In fact, this was because you have to scroll down to see the `Allow` and `Block` buttons. This isn't the case any more. You should see them.
* If acitivities are in use and there was only one activity associated with a project, the association for a new time record wasn't set correctly. This is fixed now.
* Projects can be set as inactive for some versions now. Inactive projects don't come up within the project selection. Since 1.8 inactive projects aren't shown in the project summaries any more. This helps you focusing on active projects. Furthermore this helps improving performance.
* Smaller icons for main menu tiles. They should look a bit better now. Completely new icons planned for 1.9.

### 1.7.0.0

#### Bugfixes

* Fixed "last month" calculation issue (if last month is December)
* Edit entry: Fixed update issue when chaning activity and instantly triggering save
* Fixed backup issue
* Changed turnover format, no currency symbol exported any more
* Fixed project summary and month list calculation

### 1.6.0.0

#### New features

* Inactive projects are visualized in project list
* Inactive activities are viszalized in activities list

#### Bugfixes

* Fixed database update task, app crashed when accessing projects or activities
* Fixed wrong calculation
* Fixed back handling issues

### 1.5.0.0

This version includes a lot of bug fixes as well as some new features. See the list below for more information.

#### New features

* Mark projects open/closed
* Add new time record from month list
* Mark activities as active/inactive
* Export databases
* Sorted list of projects in time record selection
* Deactivated menu bar on popups

#### Bugfixes

* Time record creation issue
* Not all month were shown in month list
* Scrolling issue on project list
* Error when deleting an activity in use
* Activies could not be updated
* "No default project" comes up every time
* Fixed German translations

### 1.4.0.0

This version is a major update and brings a lot of new features and improvements. See the list below to find out more about this release.

#### New features

* New start screen
* Break times
* Call app history directly from app
* Rate application in Marketplace
* Hourly rates
* All-inclusive price for projects
* Landscape support for add and edit page (time entry)
* Overall time is shown in month list
* Last errors are saved and can be sent via about-screen
* Manage activities and default billing rates
* Associate projects and activities (default billing rates can be overwritten)
* Time recordings from a project view
* Select projects for export

#### Improvements

* Dropbox: Updated to new authentication mode
* Upload improvements (better error messages ...)
* Added break times, activity, total time etc. to export
* New design for summary
* Updated main screen (tiles)
* Removed app bar from main screen
* Usability improvements for add and edit time entries
* If no default project is set, the first project of all projects is pre-selected
* Projects sorted ascending
* Notification when no default project defined
* Entry list now integrated in main panorama
* Better visualization of entry list
* Confirmation when cancelling tracking
* Corrected location of save and cancel buttons
* Bigger size for save and cancel icons (tracking)
* Tile uses now theme background color
* Changed SIP to email layout when entering an email address
* Confirmation when deleting a project, even if it's not in use
* Description is only visible for selected item in entries list
* Improved UI for editing projects
* Confirmation when deleting a time record
* New splash screen
* Restyled popups, removed unnecessary information
* Better performance

#### Bugfixes

* Fixed translations of project list (menu)
* Email address saved in settings
* Update tracking time when app is activated
* Fixed upload bug for German users

### 1.3.0.0

#### New features

* Default project is visualized in project list

#### Bugfixes

* Fixed problem with persistence of settings

### 1.2.0.0

#### New features

* Times for an entry via start/stop tracking can now be edited
* Updated translations

#### Bugfixes

* Better performance on initial load. The initial load was very slow when having many entries. The loading time has been reduced by 90%.
* Overview is updated when an entry has been deleted or edited

### 1.1.0.0

#### New features

* Start/stop tracking
* Create entries during active tracking
* Panorama
* Suggestions for description field
* Set project as default
* Export CSV via email

#### Bugfixes

* Error in lists when doing an action without a selection fixed
* Fixed back handling

### 1.0.0.0 - Initial release

* Add projects
* Add time records
* Monthly overview
* Export CSV to Dropbox

