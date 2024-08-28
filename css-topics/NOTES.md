# General CSS Concepts

## CSS Box Model
- CSS box model essentially is a box that wraps around every HTML element. - Every element in  CSS is considered as box.
- It consists of: content, padding, border and margin.
- Width don't consist of padding and border by default.
- Actual width of element is calculated by - combining width of padding + width of border + element's width
- The box's total width & height stops at border.


## Outline - CSS Property
- Outline is an outer line to border of box
- This doesn't include in the width of the element


## CSS Positioning
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