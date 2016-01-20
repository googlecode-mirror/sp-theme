# Introduction #

[boilerplate/boilerplate.css](http://code.google.com/p/sp-theme/source/browse/boilerplate/boilerplate.css)

[style.css](http://code.google.com/p/sp-theme/source/browse/style.css)
```
 #wrapper
 	#header
 	#content
 		#primarycontent
		#secondarycontent
 	#footer
```

# Details #

## Structure ##
A "browser reset" and a thorough set of basic element styles are declared in `boilerplate/boilerplate.css`, from the 3rd-party _Boilerplate_ CSS framework. Sp [includes the latest Boilerplate](http://code.google.com/p/sp-theme/source/browse/boilerplate/), currently svn [revision 18](https://code.google.com/p/sp-theme/source/detail?r=18).

Sp livery is written in `style.css`, and modifications are usually made there.

## Elements and explanations ##
There is one graphic asset, the subtle gray gradient across the top. A small gradient image (`img/background.png`) is set as a repeated _background_ on the _body_ element.

The _#wrapper_ div is 900 px wide, giving the overall page width divided among its children.

Within, _#content_ sets a 10 px margin. It has two child elements:

On the left, _#primarycontent_ consumes 650 horizontal px. It is of class _.hfeed_, kicking off the hAtom markup.

On the right, _#secondarycontent_ lays out what many call a "sidebar," and is 190 px wide.

16 vertical px of _#footer_ ties things off.

### Styled Buttons ###
Instead of the more traditional _input_, form buttons use the HTML _button_ element, [styled with CSS](http://code.google.com/p/sp-theme/source/browse/style.css#304).

### Microformats ###
A few classes appear in the HTML that are not mentioned in the CSS. These are the hAtom and hCard microformats classes, used (in most cases) exclusively as semantic markers, not styling handles.

The hAtom-specified _.entry-title_ class is a convenient exception. It is styled directly.

## Print ##
The `print.css` stylesheet for print media most noticeably suppresses display of the sidebar on every view, the comment form on any individual entry, and many of the theme's characteristic outline boxes.

## Gesso ##
_Gesso_ was briefly a fork of Boilerplate, still to be found in older editions of Sp. V6 users should read "gesso" for "boilerplate", above.

## See also ##
  * [CSS-Boilerplate](http://code.google.com/p/css-boilerplate), by Nathan Borror
  * _hAtom_ and _hCard_ at http://microformats.org