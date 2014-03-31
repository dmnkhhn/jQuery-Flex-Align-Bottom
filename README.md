jQuery Flex Align Bottom
===========================

This jQuery plugin provides an easy way to bottom align an element in its parent. Even if the parents height changes after resizing the browser window, in a fluid or responsive layout for example.


Usage
-----

Simply include this file in your project (after loading jQuery) like this:

<script defer src="js/jquery.flexalignbottom.js"></script>

Then call the plugin on the element which needs to be bottom aligned to it's parent.

  <script>
  $(document).ready(function() {
    $('#element-to-be-aligned').flexAlignBottom();
  });
  </script>

This will take the parents height, the elements own height and calculate the distance the element should have from the parents top to be aligned to the bottom. This value is applied to the top margin of the element by default and moves the element down.


Options
-------

You can pass an options hash to the plugin.

 - `onAttribute` - the css attribute that the value should be set on (default: 'margin-top')
 - `verticalOffset` - the number of pixels to offset the vertical alignment by, ie. 10, "50px", -100 (default: 0)
 - `parentSelector` - a selector representing the parent to bottom align this element within, ie. ".parent" (default: the element's immediate parent)

Examples:

  <script>
  $(document).ready(function() {
    $('#element-to-be-aligned').flexAlignBottom();
    $('#element-to-be-aligned').flexAlignBottom({ cssAttribute: 'padding-top', verticalOffset: '50px' });
    $('#element-to-be-aligned').flexAlignBottom({ cssAttribute: 'padding-top', parentSelector: '.parent' });
  });
  </script>


Note
----

The code is heavily based on the work of Paul Spranger. https://github.com/PaulSpr/jQuery-Flex-Vertical-Center
The initial code was more or less borrowed from the awesome FitText plugin. http://fittextjs.com/
