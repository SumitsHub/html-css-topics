# General CSS Concepts

## Table Contents
01. CSS Box Model
02. Outline - CSS Property
03. CSS Positioning
04. Pseudo Classes & Pseudo Elements
05. Media Queries
06. Variables in CSS


### 01. CSS Box Model
- CSS box model essentially is a box that wraps around every HTML element. - Every element in  CSS is considered as box.
- It consists of: content, padding, border and margin.
- Width don't consist of padding and border by default.
- Actual width of element is calculated by - combining width of padding + width of border + element's width
- The box's total width & height stops at border.


### 02. Outline - CSS Property
- Outline is an outer line to border of box
- This doesn't include in the width of the element
- NOTE: border is included in width of element by default


### 03. CSS Positioning
- position: static
  - default view
  - element positioned in the document according to the normal flow
  - no effect of top, right, bottom & left
- position: relative
  - The element is positioned according to the normal flow of the document, and then offset relative to itself based on the values of top, right, bottom, and left
  - The offset does not affect the position of any other elements; 
  - thus, the space given for the element in the page layout is the same as if position were static.
- position: absolute
  - The element is removed from the normal document flow, and no space is created for the element in the page layout
  - The element is positioned relative to its closest positioned ancestor (if any) or to the initial containing block
  - Its final position is determined by the values of top, right, bottom, and left
- position: fixed
  - The element is removed from the normal document flow, and no space is created for the element in the page layout. 
  - The element is positioned relative to its initial containing block, which is the viewport in the case of visual media. 
  - Its final position is determined by the values of top, right, bottom, and left.
- position: sticky
  - The element is positioned according to the normal flow of the document, and then offset relative to its nearest scrolling ancestor and containing block (nearest block-level ancestor), including table-related elements, based on the values of top, right, bottom, and left. 
  - The offset does not affect the position of any other elements.
  - sticky element "sticks" to its nearest ancestor that has a "scrolling mechanism" (created when overflow is hidden, scroll, auto, or overlay), even if that ancestor isn't the nearest actually scrolling ancestor.


### 04. Pseudo Classes & Pseudo Elements
#### Pseudo-classes
Pseudo-classes in CSS are used to define the special states of an element. 
They can be used to style an element when it is in a certain state, such as when it is hovered over, focused, or visited.

#### Pseudo Elements
Pseudo-elements in CSS are used to style specific parts of an element. 
They allow you to apply styles to a part of the content of an element, such as the first letter or line, or to insert content before or after an element.
Examples:
::after - p::after - Insert something after the content of each <p> element
::before - p::before - Insert something before the content of each <p> element
::first-letter - p::first-letter - Selects the first letter of each <p> element
::first-line - p::first-line - Selects the first line of each <p> element
::marker - ::marker - Selects the markers of list items
::selection - p::selection - Selects the portion of an element that is selected by a user 

#### Difference Between Pseudo-Classes and Pseudo-Elements
- Pseudo-Classes: Used to define the special state of an element. They are prefixed with a single colon (:). Examples include :hover, :focus, :nth-child, etc.
- Pseudo-Elements: Used to style specific parts of an element. They are prefixed with a double colon (::). Examples include ::before, ::after, ::first-line, etc.

#### Double colon notation - ':after' and '::after'

- :after
Single Colon (:): This is the older syntax used in CSS2.
Backward Compatibility: It is still supported by browsers for backward compatibility with older stylesheets.

- ::after
Double Colon (::): This is the newer syntax introduced in CSS3 to distinguish pseudo-elements from pseudo-classes.
Modern Standard: It is the recommended syntax for defining pseudo-elements according to the CSS3 specification.



### 05. Media Queries

#### Introduction
The @media rule, introduced in CSS2, made it possible to define different style rules for different media types.

Media queries in CSS3 extended the CSS2 media types idea: Instead of looking for a type of device, they look at the capability of the device.

Media queries can be used to check many things, such as:
- width and height of the viewport
- orientation of the viewport (landscape or portrait)
- resolution

#### Media Query Syntax
A media query consists of a media type and can contain one or more media features, which resolve to either true or false.

```css
@media not|only mediatype and (media feature) and (media feature) {
  CSS-Code;
}
```
- The mediatype is optional (if omitted, it will be set to all). However, if you use not or only, you must also specify a mediatype.

#### CSS Media Types

- all -	Used for all media type devices
- print -	Used for print preview mode
- screen -	Used for computer screens, tablets, smart-phones etc.

#### Media Features
- orientation -	Orientation of the viewport. Landscape or portrait
- max-height -	Maximum height of the viewport
- min-height -	Minimum height of the viewport
- height -	Height of the viewport (including scrollbar)
- max-width -	Maximum width of the viewport
- min-width	- Minimum width of the viewport
- width	- Width of the viewport (including scrollbar)


#### Meaning of the not, only, and and keywords:

- not: This keyword inverts the meaning of an entire media query.
- only: This keyword prevents older browsers that do not support media queries from applying the specified styles. 
  - *It has no effect on modern browsers.
- and: This keyword combines a media type and one or more media features.


#### Stylesheets specific to different media and widths
```html
You can also link to different stylesheets for different media and different widths of the browser window (viewport):

<link rel="stylesheet" media="print" href="print.css">
<link rel="stylesheet" media="screen" href="screen.css">
<link rel="stylesheet" media="screen and (min-width: 480px)" href="example1.css">
<link rel="stylesheet" media="screen and (min-width: 701px) and (max-width: 900px)" href="example2.css">
```

### 06. Variables in CSS
#### The var() Function
The var() function is used to insert the value of a CSS variable.
CSS variables have access to the DOM, which means that you can create variables with local or global scope, change the variables with JavaScript, and change the variables based on media queries.

#### Syntax of the var() Function
```css
var(--name, value)
```
Where - 
name	Required. The variable name (must start with two dashes)
value	Optional. The fallback value (used if the variable is not found)

Note: The variable name must begin with two dashes (--) and it is case sensitive!

#### Global and Local Variables
Global variables can be accessed/used through the entire document, while local variables can be used only inside the selector where it is declared.

To create a variable with global scope, declare it inside the :root selector. The :root selector matches the document's root element.

To create a variable with local scope, declare it inside the selector that is going to use it.