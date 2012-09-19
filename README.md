Style Guide
==============

Keep it Simple, Stupid
----------------------


* When you cascade a rule, keep it local and obvious.  The cascade is a powerful
  weapon in the CSS armoury, and like any weapons it should be used with caution
  and plenty of aforethought and planning.
* Define a list of global rules which have no side effects in a global context,
  for example 'active', 'first', 'last'
* Favour pixels as units, em's in the case of typographic relativity (% is
  derived and in pixels, line-height is unitless, pixels or em's). Pixels are
  clear, work everywhere and have no unwanted zooming side effects.
* Constrain component variations, eg. 4 header styles only, 2 list styles, etc

Separation of Concerns
----------------------

* An H1 is not a style. Create a language for typography ( and there's no harm
  in verbosity if it's self documenting):
  ** .foo-heading-title { /* foo is the namespace */ }
  ** .foo-heading-main { }
  ** .foo-heading-medium { }
  ** .foo-heading-small { }
  ** .foo-heading-runin { }
* Prefix grid, js, style, rules, eg. grid-, js-, style- and keep them seperate. 
* Each namespace should be agnostic to the styles in another namespace.
* A page is not a style, consider carefully body class styles.
* Prefer a multiclass pattern over the cascade. 

Do not Repeat Yourself
----------------------

* Modularise components. A component should be able to work with no side effects
  on any page, it's CSS should be clearly labelled and identifiable with that
  component. (See headers example)
* A header style, list style, table style, whatever, should work once and
  everywhere the same.
* Leverage CSS Preprocessors, but keep it simple.
