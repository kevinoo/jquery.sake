jQuery.sake
===========

Collection of some utility for web development, extending the collection methods of the jQuery library (http://jquery.com/download/).

Features:

##### $.fn.scrollTo( speed, easing )
Performs scrolling the page using the parameters passed (or the default)
```javascript

// Scroll to the element using default params (500ms of speed and linear easing)
$('#to_element').scrollTo();

// Overwrite params
$('#to_element').scrollTo( 500, 'linear' );

// Overwrite params using an object
$('#to_element').scrollTo({
    'speed': 500,
    'easing': 'linear'
});
```

##### $.fn.validate(method, params)
Checks if the fields into *selector* are valid: returns true if are valid else returns false.
```html

<div id="box_to_validate">
    Everything value is allowed (also empty text): <br />
    <input type="text" data-info="everything_value_is_allowed"> <br /><br />

    No allowed an empty value: <br />
    <input type="text" data-info="everything_value_except_the_empty_field" data-cmp="true"> <br /><br />

    Text at least 3 chars: <br />
    <input type="text" data-info="must_be_a_text_at_least_3_chars" data-cmp="true" data-type="text" min="3"> <br />
    <input type="text" data-info="must_be_a_text_at_least_3_chars" data-cmp="true" data-type="text" data-min="3"> <br /><br />

    Hidden input with a happy value:
    <input type="hidden" data-info="my_key" data-cmp="true" value="Smile! Here there is Sake!"> <br /><br />
</div>
```
```javascript
// Check fields inside the box - Returns FALSE if at least one is empty

if( $('#box_to_validate').validate() === false ){
    alert('Error in fields');

    // To retrieve invalid fields :)
    var $invalid_fields = $('#box_to_validate').find('.invalid');

    return;
}

var data_in_box = $('#box_to_validate').getDataInfo();

// What is in *data_in_box* variable:
// {
//     'everything_value_is_allowed': '',
//     'everything_value_except_the_empty_field': 'test text',
//     'must_be_a_text_at_least_3_chars': 'something is happy',
//     'my_key': 'Smile! Here there is Sake!'
// }
```

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

##### $.fn.realOuterWidth(includeMargin)
Return a width of an element (also hidden)

##### $.fn.realOuterHeight(includeMargin)
Return a width of an element (also hidden)

##### $.fn.getDataInfo(delimiter, ignoreHidden, types)
Returns an object with field data inside the $container (*selector*)
```html

<div id="box_to_validate">
    Everything value is allowed (also empty text): <br />
    <input type="text" data-info="everything_value_is_allowed"> <br /><br />

    No allowed an empty value: <br />
    <input type="text" data-info="everything_value_except_the_empty_field" data-cmp="true"> <br /><br />

    Text at least 3 chars: <br />
    <input type="text" data-info="must_be_a_text_at_least_3_chars" data-cmp="true" data-type="text" min="3"> <br />
    <input type="text" data-info="must_be_a_text_at_least_3_chars" data-cmp="true" data-type="text" data-min="3"> <br /><br />

    Hidden input with a happy value:
    <input type="hidden" data-info="my_key" data-cmp="true" value="Smile! Here there is Sake!"> <br /><br />
</div>
```
```javascript
// Check fields inside the box - Returns FALSE if at least one is empty

if( $('#box_to_validate').validate() === false ){
    alert('Error in fields');

    // To retrieve invalid fields :)
    var $invalid_fields = $('#box_to_validate').find('.invalid');

    return;
}

var data_in_box = $('#box_to_validate').getDataInfo();

// What is in *data_in_box* variable:
// {
//     'everything_value_is_allowed': '',
//     'everything_value_except_the_empty_field': 'test text',
//     'must_be_a_text_at_least_3_chars': 'something is happy',
//     'my_key': 'Smile! Here there is Sake!'
// }
```

##### $.fn.setDataInfo(data, options)
Set data-info attribute to children of $container (*selector*)
```javascript

$('#box_to_validate').setDataInfo({
    'everything_value_is_allowed': 'Blaaaaa :-)',
    'everything_value_except_the_empty_field': 'text test',
    'must_be_a_text_at_least_3_chars': 'happy is something',
    'my_key': 'Here there is Sake! Smile!'
});
```

##### $.fn.checkboxes(action)
Trigger an action to checkboxes contain in a $container (*selector*)
```html
<div id="my_checkboxes_box">
    <input type="checkbox" id="a" value="1"> <br />
    <input type="checkbox" data-info="a" value="2"> <br />
    <input type="checkbox" data-info="b" value="3" checked="checked"> <br />
</div>
```
```javascript

$('#my_checkboxes_box').checkboxes('values');
// [3]
// Only last checkbox is checked :P

// Invert selection of all checkboxes
$('#my_checkboxes_box').checkboxes('invert');
```