jquery.sake
===========

Collection of some utility for web development, extending the collection methods of the jQuery library (http://jquery.com/download/).

Features:

##### $.fn.scrollTo(params, easing)
Perform a scroll to a element

##### $.fn.getAllStyle(attrs, no_obj)
Return an object with all css styles of *selectora*

##### $.sakelightbox(method, params)
Show a lightbox in the window.

##### $.fn.setPositionTo(eleTo, params)
Set the position of *selector* to another element (selector).

##### $.fn.tooltip(method, params)
Show a tooltip near the element (*selector*), customizable with params

##### $.fn.validate(method, params)
Checks if the fields into *selector* are valid: returns true if are valid else returns false.

##### $.fn.check(type, subtype)
Check the data into the *selector* (input or select).

##### $.fn.escape()
Return the value of the *selector* escaped.

##### $.escape(str)
Return the string "str" escaped

##### $.fn.replace(search, replacement, modifier)
Replace the text *search* (can be a regular expression) in the *selector* with the *replacement*.

##### $.fn.lorem(params, length, random)
Write in the *selector* a lorem text

##### $.fn.random(params)
Hide or remove randomly a "count" element inside of $container (*selector*)

##### $.fn.getEvents()
Return a map of events associated at element

##### $.fn.hash()
Return the hash of the selector's value

##### $.fn.sakebuttons(params)
Create a button ON/OFF in Android style

##### $.fn.whenChange(method, params)
Check the content of the element and trigger the event "change" on it

##### $.fn.trim()
Replace and returns the value of *selector* with the value "trimmed"

##### $.fn.template( where, data, appendTo, extraData )
Copy in a template the data passed and append to element selected (where)

##### $.fn.blink(method, params)
Apply a blink effect to the element

##### $.fn.realOuterWidth(includeMargin)
Return a width of an element (also hidden)

##### $.fn.realOuterHeight(includeMargin)
Return a width of an element (also hidden)

##### $.fn.getDataInfo(delimiter, ignoreHidden, types)
Returns an object with field data inside the $container (*selector*)

##### $.fn.setDataInfo(data, options)
Set data-info attribute to children of $container (*selector*)

##### $.fn.checkboxes(action)
Trigger an action to checkboxes contain in a $container (*selector*)

##### $.tips(method, params)
Show a tip in the window (default: bottom right).

##### $.loop(params, howmany, delay)
Run a function many times with a optional delay


