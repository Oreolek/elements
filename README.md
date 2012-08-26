LESS Elements
=============

LESS Elements is a set of useful mixins for the [LESS CSS pre-processor](http://lesscss.org) to help you cut down the size of your stylesheets.

LESS is a fantastic tool that extends CSS and makes writing and maintaining large stylesheets easy. Even so, I found myself re-writing the same mixins again and again for different projects. LESS Elements is a collection of these common re-usable mixins.

For example, let’s look at a bit of CSS3 code that adds a couple of rounded corners (only the top left and top right edges):

    #some_div {
      -webkit-border-top-left-radius: 5px;
      -webkit-border-top-right-radius: 5px;
      -moz-border-radius-topleft: 5px;
      -moz-border-radius-topright: 5px;
      border-top-left-radius: 5px;
      border-top-right-radius: 5px;
    }

Browser specific code makes using CSS3 a chore. 6 lines of code just to add rounded corners. LESS mixins to the rescue. With LESS Elements the above can be compressed to just a 1 line:

    #some_div {
      #border > .radius(5px, 0, 0, 5px);
    }

Looks just line shorthand CSS, with the values representing top right, bottom right, bottom left and top left corner radii in a clockwise order. To use LESS Elements, just download it (Github repo), put the “elements.less” file in your stylesheets folder and include it with 1 line of code at the top of your LESS file:

    @import "elements";
    
Currently LESS Elements includes following namespaces:

[Gradients](https://github.com/Oreolek/elements/wiki/Gradients)

[Borders](https://github.com/Oreolek/elements/wiki/Borders)

[Shadows](https://github.com/Oreolek/elements/wiki/Shadows)

[Transformations](https://github.com/Oreolek/elements/wiki/Transformations)

[Transitions](https://github.com/Oreolek/elements/wiki/Transitions)

[Layout](https://github.com/Oreolek/elements/wiki/Layout)