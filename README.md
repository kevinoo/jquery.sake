jquery.sake
===========

Collection of some utility for web development, extending the collection methods of the jQuery library (http://jquery.com/download/).

Features:

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

##### $.fn.hash()
Return the hash of the selector's value

##### $.fn.trim()
Replace and returns the value of *selector* with the value "trimmed"

##### $.fn.template( where, data, appendTo, extraData )
Copy in a template the data passed and append to element selected (where)

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
