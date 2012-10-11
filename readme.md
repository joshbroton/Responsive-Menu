# jQuery Responsive Menu Plugin
A Plugin which turns your site's navigation into a dropdown (<`select>`) when your browser is at mobile widths.

##Changelog
1. Added support for target="_blank" on links in the menu. This can be turned off by setting honorTargetBlank to false.
2. Added support for window.matchMedia(). It now defaults to this and falls back to the comparing switchWidth to $(window).width() because of the differences in the way Firefox and IE10 implement .width() vs. all media queries. IE8 doesn't support window.matchMedia(), but that's OK because it measures .width() the same way as media queries.
3. Changed the way the top level menu items are converted into links with the text from groupPageText. If that top level menu item doesn't contain a link (which it shouldn't due to touch devices), then it doesn't create the "dummy" `<option>`.
4. Minor speed enhancements.

## Options
The options available for the plugin are listed below.
Their default value appears next to their names, and available values below the description.

### combine [true]
Convert multiple navigation lists into a single dropdown for mobiles
[true/false]

### groupPageText ['Main']
Any `<li>` elements with `<ul>/<ol>` present get converted to an `<optgroup>`.
As `<optgroup>` isn't selectable, a "dummy" `<option>` is added at the top of the group with the `<li>`'s value.
This option sets the text for the "dummy" `<option>`
['string']

### nested [true]
This turns the `<optgroup>`s on and off
[true/false]

### prependTo ['body']
Sets the container element for the menu to be put into.
['CSS-selector']

### switchWidth [480]
Sets the width (in pixels) at which the site's menu(s) will change to a `<select>`

### topOptionText ['Select a page']
Sets the very first `<option>`'s display text.
Setting this to NULL will prevent it from displaying
['string'/null]

### honorTargetBlank [true] **new
Carry over the functionality of any target="_blank" that you've put on your menu links.

## Usage
The plugin can be used like any other jQuery plugin:

$('css-selector').mobileMenu({option:value, option:value});

## Licence
There isn't one, because I'm nice.
Feel free to say "thanks" or attribute the script to this page if you find it useful.