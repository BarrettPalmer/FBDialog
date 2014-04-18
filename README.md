FBDialog
========

jQuery Facebook Dialog Plugin

View the [Demo](http://www.rrpowered.com/demo/FBDialog/)

Usage
-----

Include the latest jQuery library, the fbdialog.css and the FBDialog plugin.
```HTML
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/2.1.0/jquery.min.js"></script>
<script type="text/javascript" src="fbdialog.min.js"></script>
<link rel="stylesheet" href="fbdialog.css" />
```

As a chained jQuery function, you can call the `fbdialog()` function on a jQuery element and a modal dialog will be displayed using the contents of that element. For example:
```JAVASCRIPT
$("#your-element-id").fbdialog();
```

Options
-----
Replace `options` text in the plugin with the option listed below.

```JAVASCRIPT
$("#your-element-id").fbdialog({options});
```

The title, cancel button, okay button’s text can be changed. Okay button and cancel button can be removed from dialog. The opacity and dialog top position can be changed using the dialog option.
Below is a list of the plugin options:
```JAVASCRIPT
        title: "YOUR TITLE HERE",   Dialog title text
       cancel: "Cancel",            Cancel button text
         okay: "Okay",              Okay button text
   okaybutton: true,                show the ok button
 cancelbutton: true,                Show the cancel button
      buttons: true,                Show the buttons
      opacity: 0.0,                 The opacity value for the overlay div, from 0.0 - 1.0
    dialogtop: "78px",              Position of dialog from top of page  0px - 99999px
```

Callback functions
-----
Use the `callback` function to know when the Okay button or Cancel button are clicked.
Example:
```JAVASCRIPT
$(".div").fbdialog({
        title: "Facebook Dialog",
    },
    function (callback) {
        if (callback == 1) {
            alert("Okay button clicked.");
        }
        if (callback == 2) {
            alert("Cancel button clicked.");
        }
    });
```

Closing the dialog
-----
You can use a `id` or `class` for the element selector. Example below:
```HTML
<a href="#" id="fbclose">Close this dialog</a>
```
Use the code below to close the dialog with a class or id. The plugin uses jQuery’s `on` method instead of `click` method because the id or class used on the link for closing of the dialog are added after the `DOM` has loaded.
 
Inside the `on` method’s function, simply add the id or class selector of the dialog with the option `close: true`

```JAVASCRIPT
$(document).on("click", "#fbclose", function() {     
    $("#your-element-id").fbdialog({close: true});
});
```
[Demo](http://www.rrpowered.com/demo/FBDialog/)
