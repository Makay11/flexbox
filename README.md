# @makay/flexbox

[![npm (scoped)](https://img.shields.io/npm/v/@makay/flexbox.svg?style=flat-square)](https://www.npmjs.com/package/@makay/flexbox)
[![license](https://img.shields.io/github/license/Makay11/flexbox.svg?style=flat-square)](http://opensource.org/licenses/ISC)

Tiny flexbox library (1.70KB gzipped) to help you build responsive layouts quickly and without writing any CSS.

Goals of this library:

- To expose most of flexbox's properties as human-readable CSS classes.
- To not change any properties of classes/elements outside the library.
- To be able to be used alongside other CSS libraries and frameworks without breaking anything*.
- To be as small as possible while still achieving all the previous goals.

*\* There might be collisions with the class names of some libraries or frameworks (like Bootstrap's ".row"). If possible, exclude the grid systems offered by these as you will not be needing them anyway. If you really have to keep them, make sure this library is loaded after them and things might still work for the most part.*

# What is flexbox?
> Flexbox provides tools to allow rapid creation of complex, flexible layouts, and features that historically proved difficult with CSS. [[Source](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox)]

If you're unfamiliar with flexbox be sure to take a look at the following resources (in no specific order):

- http://cssreference.io/flexbox/
- https://css-tricks.com/snippets/css/a-guide-to-flexbox/
- https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox
- https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox

# Installation

## npm (recommended)

Run `npm install @makay/flexbox` or `yarn add @makay/flexbox` to install the latest version.

Include `node_modules/@makay/flexbox/flexbox.css` or `node_modules/@makay/flexbox/flexbox.min.css` in your bundle using your preferred bundler.

## CDN

Include  one of the following stylesheets in your page:

https://cdn.jsdelivr.net/npm/@makay/flexbox@1.0.4/flexbox.css

https://cdn.jsdelivr.net/npm/@makay/flexbox@1.0.4/flexbox.min.css

# Documentation

After installing the library, you can start using it by adding the classes listed below to the elements of your page.

## Container classes

Class|CSS properties
---|---
row|display: flex;<br>flex-shrink: 0;<br>flex-direction: row;
column|display: flex;<br>flex-shrink: 0;<br>flex-direction: column;

### Container modifiers

Class|CSS properties
---|---
reverse|flex-direction: row-reverse;<br>**or**<br>flex-direction: column-reverse;
shrink|flex-shrink: 1;
wrap-reverse|flex-wrap: wrap-reverse;
wrap|flex-wrap: wrap;
nowrap|flex-wrap: nowrap;
align-start|align-items: flex-start;
align-center|align-items: center;
align-end|align-items: flex-end;
align-baseline|align-items: baseline;
align-stretch|align-items: stretch;
align-content-start|align-content: flex-start;
align-content-center|align-content: center;
align-content-end|align-content: flex-end;
align-content-stretch|align-content: stretch;
align-content-space-between|align-content: space-between;
align-content-space-around|align-content: space-around;
justify-start|justify-content: flex-start;
justify-center|justify-content: center;
justify-end|justify-content: flex-end;
justify-space-between|justify-content: space-between;
justify-space-around|justify-content: space-around;

## Child classes

Class|CSS properties
---|---
*(any)*|max-width: 100%;
align-self-auto|align-self: auto;
align-self-start|align-self: flex-start;
align-self-center|align-self: center;
align-self-end|align-self: flex-end;
align-self-baseline|align-self: baseline;
align-self-stretch|align-self: stretch;
flex-none|flex: none;
flex|flex-grow: 1;
flex-**X**|flex-basis: calc(**X***100%/12);

***X** can range from 1 to 12, inclusive.*

### Child media queries

Class|max-width|CSS properties
---|---|---
flex-lg-**X**|1919px|flex-basis: calc(**X***100%/12);
flex-md-**X**|1279px|flex-basis: calc(**X***100%/12);
flex-sm-**X**|959px|flex-basis: calc(**X***100%/12);
flex-xs-**X**|599px|flex-basis: calc(**X***100%/12);

***X** can range from 1 to 12, inclusive.*

## Utility classes

Class|CSS properties
---|---
padded|padding: 16px;
hidden|display: none;

### Utility media queries

Class|max-width|CSS properties
---|---|---
hidden-lg|1919px|display: none;
hidden-md|1279px|display: none;
hidden-sm|959px|display: none;
hidden-xs|599px|display: none;

Class|min-width|CSS properties
---|---|---
hidden-gt-lg|1920px|display: none;
hidden-gt-md|1280px|display: none;
hidden-gt-sm|960px|display: none;
hidden-gt-xs|600px|display: none;

# Contribute!
Found an issue or want to add a new feature? Feel free to open an issue or make a pull request!
