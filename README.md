# Qlik Sense extension for field and variable selections with "missing features"

This extension is an "all in one" selection component with several customization options. It gives you many Qlikview features like select only one, default value and context menu.
To reduce amount of required extensions on a sheet Simple Field Select has global options for the current sheet, for example you can set background color of the sheet, hide title bar, modify all borders etc. You can hide these settings for example inside the year selector.

If you have a good idea for further development, let us know.

## To install
Download a ZIP file from the dist directory or clone the branch. Install the zip as any Qlik Sense extension.

## Latest features
- Note! Change to export mode handling in 1.8.6, see release notes
- Responsive font size options
- Menu icon styled right click menu trigger - if export mode is used, right click menu won't work
- Gloabl options for hiding Smart search, Selections tool and new Insights buttons from the toolbar
- Leonardo UI styled Radio button
- Only text object visualization. Use CSS, Javascript and HTML on a text box. This was implemented because most of the SFS settings can be reused, like color, header and global settings.
- Global option to hide pivot tables "boxes" - frees a lot of space
- Global option to add extra text field to sheet header and selections bar - use for example to show document update time, current user etc

## Features
- supports **select only one** and **default value(s)** selection - so when you enter to a document or a sheet, you can have default value/values selected
- Has a context menu (right click menu) for _select all_, _clear selections_, _reverse selection_, _select possible_, _select default values_ and _select randomly_ (Just came to my mind, for fun maybe). You can select which options are shown on the menu.
- will fit on one line - you can disable Qlik Sense default header, paddings, margins and do other tricks to enhance standard visualization
- renders as a list, button row, checkbox, standard radio button or drop down selector.
- For variable control there is now almost every HTML5 standard input
  - For example slider
- custom text fields: label text, tooltip for mouse hovering and help text below the element
- can set variable value from predefined list or via date picker
  - two variables can be set at the same selection (if you need a value for UI and value for other usage)
  - date picker can limit to min and max date
- mobile zoom effect can be disabled. No need for three clicks if you want to select something. **Only one click is enough!!**
- several posibilities for visual changes like colors, borders etc. Custom CSS classes, HTML attributes can be applied to rendering. In this way you can use for example CSS classes from other libraries to render elements.
- supports hiding a field from Qlik Sense's selection row
- supports transparency of the object
- Some of the visualizations allow to use Qlik Sense's Leonard UI styling, for example for drop down select Leonard UI styling works well
- search can be enabled for some of the visualizations
- background color for the object itself
- Hide all headers from a sheet + color options for every header
- Qlik Sense styled switch and checkbox
- Dropdown can be now used as multiselect. Naturally doesn't work with variables
- Select2 plugin has been integrated to the extension. It allows to use a searchable dropdown menu, either normal version or multiselect version.

## Global sheet level settings
All following global settings are sheet specific. You can use for example master items if you wan't to have the same settings on same element on every sheet.

- Global parameters for a sheet:
  - Modify background color of the sheet and all objects.
  - Change border style for all objects on the sheet.
  - Hide any field(s) from the selection bar.
  - Hide sheet title or modify it's size and font-size
  - Hide selections bar and main menu bar. But be carefull if you remove the main menu, you can access edit mode only by changing the end of the url to /state/edit
  - Hide header from the Text & Image objects. You will get much more space for the text itself! Many times users cannot see the text because of the size of the header in the text object so now you can get rid of it!
  - Hide header from every object on a sheet
  - Reduce header padding in all objects while using Focus theme
  - Font-family and font color can be set for all elements
  - Remove filter boxes from Pivot tables
  - Extra text field to selection bar and header
  - Hide pivot table filter boxes for space
  - Hide Smart search, Selections tool and Insights buttons


This extension is supposed to be very light weight. It has no big libraries attached to it. In this way your Qlik Sense application is able to stay as fast as possible.
Note that some text field allow Qlik developer to write javascript, HTML and CSS.

### Changelog
[ChangeLog](ChangeLog)

## Screenshots
![Examples](/docs/img/select2demo.PNG?raw=true "Header and Select2 demo" )

![Examples](/docs/img/SFSdemo.JPG?raw=true "Examples" )

![Settings](/docs/img/SFSselections3.PNG "Visual example" )

And context menu for the "missing features":

![Context menu](/docs/img/contextmenu.PNG "Context menu" )

![Context menu](/docs/img/luidemo.png "Switch and checkbox Qlik style" )

HTML inputs:

![HTML5](/docs/img/html5examples.PNG "HTML5 standard inputs" ) ![HTML5](/docs/img/html5examples2.PNG "HTML5 standard inputs" ) ![HTML5](/docs/img/html5Example3.PNG "HTML5 standard inputs" )


For date picker jQuery UI component is used. CSS is parsed for only required parts.
Select2 (select2.org) plugin is used for Select2 dropdown visualization.
