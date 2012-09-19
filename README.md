Style Guide
==============

Style Guide sandbox: http://jsbin.com/ifefoq/latest

Keep it Simple
--------------

* When you cascade a rule, keep it local and obvious.
* Define a list of global rules which have no side effects in a global context,
  for example 'active', 'first', 'last', 'hide' (that is to say, you shouldn't
  create classes like this without thinking long and hard!)
* Favour pixels as units, em's in the case of typographic relativity (% is
  derived and in pixels, line-height is unitless, pixels or em's). Pixels are
  clear, work everywhere and have no unwanted zooming side effects.
* Constrain variations, eg. 4 header styles only, 2 list styles, 1 table style
  etc etc
* Define the physical world your components live in, don't keep coming up with
  shadow depths, angles, radii, easing types. Make it consistent and learnable. 

Separation of Concerns
----------------------

* Separate the element from the style, HTML from CSS. An H1 is not a style.
  Create a language for typography ( and there's no harm in verbosity if it's
  self documenting):
    * .foo-heading-title { /* foo is the css namespace */ }
    * .foo-heading-main { }
    * .foo-heading-medium { }
    * .foo-heading-small { }
    * .foo-heading-runin { }
* Prefix grid, js, style, rules, eg. grid-, js-, style- and keep them seperate. 
* Each namespace should be agnostic to the styles in another namespace.
* A page is not a style, consider carefully body class styles.
* Use multiclass pattern over cascading where sensible. (Don't allow your
  component's style to leak to global) 

Do not Repeat Yourself
----------------------

* Modularise components. A component should be able to work with no side effects
  on any page, it's CSS should be clearly labelled and identifiable with that
  component. (See headers example)
* A header style, list style, table style, whatever, should work once and
  everywhere the same.
* Leverage CSS Preprocessors, but remember to keep it simple.


* * *

Code Style Guides
=================

* HTML & CSS: http://google-styleguide.googlecode.com/svn/trunk/htmlcssguide.xml
* JavaScript: http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml 
