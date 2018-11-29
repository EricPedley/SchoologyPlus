# Changelog

## Version 4.2 - November 21, 2018

### Added
- Fully-featured theme editor!
  - A more user-friendly way to customize your Schoology appearance
  - Access the theme editor through Schoology Plus settings (it replaces the old theme selection dialog)
  - Allows you to create, import, edit, export, delete, preview, and apply themes
  - Live preview of themes!
- Points possible values are shown for assignments that do not yet have a grade
  - By default, Schoology hides this information from you and shows simply an em dash (—) for assignments without a grade
- "See Archived" button in courses dropdown to quickly access archived courses
  - There is also a new setting that allows you to disable this feature

### Changed
- The Firefox extension download page now ensures you are using Firefox before downloading
- Renamed the "Custom Color" theme to "Schoology Plus"
- Renamed "Course Aliases" to "Nicknames"
- Moved document tooltips on materials pages from the file size to the file name
- New release nags
  - The "!!" on the Schoology Plus settings button and the flashing "New Update" text have been removed
  - Replaced with less intrusive on-page notification
- Theme JSON format updated
  - Themes will be automatically converted
  - Importing the old format still works
- Contributors page now more thoroughly lists icon authors
- More prominently featured Glen Husman, the co-lead developer of this extension

### Deprecated
- The "Custom Color" theme and the "Color Hue" setting have been deprecated
  - If you are currently using the Custom Color theme with a modified hue setting, your interface will remain unchanged
  - However, you are no longer able to modify the color hue setting
  - If you want to change the color, create a new theme and change the color hue

### Fixed
- Schoology Plus broadcasts now show up on https://lms.lausd.net/home
  - Previously, broadcasts would only show up on https://lms.lausd.net/home/recent-activity
- Better error handling all around
- Desktop notifications now work in Firefox

## Version 4.1.1 - September 16, 2018

### Fixes
- Address Firefox addon publishing complaints regarding old library versions

## Version 4.1 - September 16, 2018

### Changes
- "Loading..." tooltips now immediately appear for documents and assignments
- Material tooltips now generate in materials under folders (and other cases where not all materials show up at page load)
- Changelog, update, and notification infrastructural URLs updated to use GitHub pages (maintainable by all project contributors)

### Fixes
- Custom course aliases apply even with an extra space in the full name, most notably in Upcoming events
- Course dashboard fixes for custom aliases and icons
- Aliases now work properly for archived courses
- Classes without "PERIOD N" in the name will no longer crash the grades page

## Version 4.0 - September 4, 2018

### Additions
- Course aliases
  - Friendly nicknames can now be set for courses, replacing `AP ENG LANG A: TERM AF - PER 1` with nicer names, like "English (P1)"
  - Course aliases are used everywhere the full course name would be used
  - Available as a new setting in Course Options
- Material tooltips
  - The "Materials" page for each course now has tooltips for graded items and for documents
  - Graded items show the grade, what category the assignment is in, and if it has been submitted online
  - Documents (hovering over the size indicator) now show their length in pages and a preview of the first page

### Changes
- Astronomy now has a custom course icon in the default theme
- To facilitate new features such as document tooltips, new permissions are required: the extension now needs access to all of schoology.com

### Fixes
- Custom course icons apply more reliably and in more contexts
- API key retrieval, used for functions like getting denominators of missing assignments or the materials page tooltips, is now more reliable, especially for accounts which had not previously generated API keys

## Version 3.17 - August 16, 2018

### Additions
- Added option to keep teacher-provided course icons
  - Enabling this option will keep icons provided by teachers while still replacing default icons with custom SchoologyPlus icons
  
### Fixes
- Fixed the settings drop-down menu (in the top right corner) in Firefox

## Version 3.16 - May 19, 2018

### Additions
- Gradebook courses now have a context menu, linking to all course subpages
- Assignments now have a context menu
  - Can drop or undrop assignments to simulate impact on grade
  - Can calculate minimum scores on assignments needed to get a certain course letter grade (uses Schoology Plus-configured grading scale)

### Fixes
- Dropped assignments now correctly contribute to score totals
- Dropped assignments now no longer alter total score when edited while dropped
- More reliable loading of missing assignment information

## Version 3.15.2 - May 7, 2018

### Fixes
- If a maximum score for a missing assignment cannot be found, grade loading no longer hangs indefinitely

## Version 3.15 - May 3, 2018

### Additions
- Added course icons to the Course Dashboard page
- Missing assignments now show the max possible points on the grades page

### Changes
- Grade modification now allows negative point denominators
  - Use this as a way to drop assignments until proper support for this is added
  - For example, to drop an assignment with a score of 3/20, add an assignment with -3/-20 as the score
- Classes with missing assignments will take slightly longer to load, and "LOADING" may be shown while missing assignments are being processed
  - This is a result of the bug fix listed below

### Fixes
- Grade modification now respects missing assignments and counts their maximum points properly

## Version π - March 14, 2018

> The following new features were **suggested by users**. If you want your idea to be implemented into Schoology Plus, [fill out this survey](https://goo.gl/forms/iP6GzLqNc6YQoJo83). Thanks for your support and your suggestions!

### Additions
- Added a "Course Settings" menu on course pages for course-specific settings
- Added ability to create custom grading scales for each course
	- To set the grading scale, go to the page for a course and click "Course Settings" in the sidebar
	- This allows the usage of any number of custom grading symbols
- Added the ability to configure receiving announcements separately from assignment notifications
	- Previously, if notifications were disabled, announcements would not be received
	- There are three options for this setting:
		- **Enable Announcements**: Show desktop notifications and news feed posts for announcements
		- **Announcement News Feed Posts Only**: Only show posts in the news feed for announcements (no notifications)
		- **Disable Announcements**: Entirely disables checking for announcements

### Changes
- The "Assume Grading Scale" setting has been replaced with "Custom Grading Scales"
	- The default value for this new setting is `Enabled` and is not affected by the value of the old setting

### Fixes
- Fixed desktop notifications not working whatsoever on Firefox

## Version 3.10 - March 6, 2018

#### Additions

- Added broadcasts
  - Broadcasts are push notifications sent to all Schoology Plus users
  - Broadcasts are shown as desktop notifications as well as posts pinned to the top of the news feed
- Added broadcast for new users

## Version 3.9.6 - February 21, 2018

#### Fixes

- Fixed the arrow dropdown menu in Firefox
- Fixed the alignment of course icons on the mastery page

## Version 3.9.5 - February 13, 2018

#### Additions

- Added Firefox support
  - [Download Here](http://aopell.me/projects/schoology-plus-firefox-download.html)

#### Changes

- Changed the portion of the settings window that scrolls to not include the save button
- Minor behind-the-scenes changes to allow a Firefox port

## Version 3.9 - February 9, 2018

#### Additions

- Added course icons (if enabled) to the grades screen

#### Fixes

- Fixed an issue with the course icon for film classes

## Version 3.8 - February 4, 2018

#### Additions

- Course Icons
  - A default set of course icons has been added
  - These can be enabled (default) or disabled with the "Override Course Icons" setting
  - Course icons are **themeable** (See the [theme spec](https://github.com/aopell/SchoologyPlus/tree/master/themes) for details)
  - ***If your course is missing an icon, please send feedback including your course's transcript name and an icon will be added***
- Added setting to control class sort order
  - Options are `By Period` to order by period number or `Alphabetically` for the Schoology default
- Added an "Export Theme" button for custom themes
  - This will copy the theme's JSON representation to your clipboard for easy sharing
- Classes are now sorted according to your chosen sort method on the mastery page

#### Changes

- When a custom theme is added, it is immediately set as the current theme
- Removed ability to add themes with duplicate names

#### Fixes

- Settings now show their correct value when the settings page is reopened without a refresh
- Cursor image is now properly removed when switching from a theme with a custom cursor to a theme without one
- Modal styling is no longer broken on course and user pages
- Modals now resize appropriately in small windows

## Version 3.7 - January 30, 2018

#### Additions

- Added ability to change the logo image in custom themes

## Version 3.6.1 - January 29, 2018

#### Additions

- Added the ability to create custom themes
  - Currently this functionality is fairly limited
  - To create and delete custom themes, go to `Settings > Theme > Install and Manage Themes...`
  - You can install a theme by inputting JSON in the format defined [here](https://raw.githubusercontent.com/aopell/SchoologyPlus/master/themes/example-theme.json)
  - More functionality as well as a theme editor website will be added soon
  
#### Fixes

- Fixed some issues with unsaved settings persisting when the settings window was closed

## Version 3.5.2 - January 28, 2018

#### Fixes

- Fixed multiple issues related to grade modification

## Version 3.5.1 - January 27, 2018

#### Fixes

- Fixed an issue with calculating modified grades when a class had a weighted category with no assignments 

## Version 3.5 - January 26, 2018

#### Additions

- Added ability to disable grading scale assumption in settings
- Added "Feedback" link to settings page footer
  - Use this to submit bugs and feature requests

#### Changes

- The "!!" on the Schoology Plus icon now disappears when the setting screen is opened
  - However, the "New Update" indicator will persist until it is clicked

## Version 3.4 - January 23, 2018

#### Additions

- Added "LAUSD Orange" theme
- Added "Toy" theme (special thanks: :crown:)

## Version 3.3 - January 23, 2018

WARNING: *This update resets your rainbow mode setting*|
-|

#### Additions

- Added a "Theme" setting
- Added a "Restore Defaults" button to the settings page

#### Changes

- Rainbow mode is now the "Rainbow" theme
- Improved Rainbow theme for better color transitions between pages
  - The color no longer resets to red every time you load a new page

## Version 3.2 - January 20, 2018


#### Additions

- Courses drop-down no longer has a scrollbar
- Added contributors page
- Added changelog
  - Added indicator to changelog link when extension updates

#### Fixes

- Fixed number badge not showing any notifications

## Version 3.1 - January 16, 2018

#### Additions

- Added ability to disable notifications
- Added grades page link to navigation bar
- Added informational hover text to setting modified asterisk

#### Changes

- Minor improvements to options menu

#### Fixes

- Fixed options appearing modified after closing options menu without saving

## Version 3.0.2 - January 15, 2018
#### Fixes

- Bug fixes

## Version 3.0 - January 15, 2018
#### Additions

- Added options menu
- Added ability to customize navigation bar color
- Added rainbow mode

#### Changes

- Changed how notifications are checked
- Clicking notifications now takes you to the notification page

## Version 2.1.3 - December 14, 2017
#### Fixes

- Bug fixes

## Version 2.1 - December 12, 2017
#### Additions

- Added ability to simulate adding a new assignment to a category
- Added desktop notifications for new grades
- Clicking the extension icon opens Schoology

#### Fixes

- Fixed issue with hover color of home link on the navigation bar when on the home page

## Version 2.0 - December 9, 2017
#### Additions

+ Added ability to simulate changing a grade

#### Fixes

* Fixed gap in darker color when hovering over links on the navigation bar

## Version 1.2.3 - December 8, 2017
#### Fixes

- Bug fixes

## Version 1.2 - December 8, 2017
#### Additions

- Classes are now sorted by period

## Version 1.1 - December 8, 2017

#### Additions

- Added letter grades for classes that don't set them (assumes 10% grading scale)
- Schoology logo can now be clicked to return to the home page

## Version 1.0.1 - December 7, 2017

#### Fixes

- Fixed dropped grades counting in point totals