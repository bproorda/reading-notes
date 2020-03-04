5[Home](README.md)

# HTML Layout
- CSS treats each HTML as if it is in own box, they will be either block or inline elements.
- block elements always start on a new line
- inline elements flow around surrounding text
- if a block level element sits inside a block level element, the latter is the parent.
- css has the following positioning schemes
  - normal flow: every block is on a new line, no matter the width setting
  - relative positioning: shifts an element based on where it would have appeared in the normal flow, does not effect surrounding elements.
  - absolute positioning: positions element in relation to its containing element. element is taken out of normal flow. elements move when window is scrolled
  - fixed: positions element in relation to the browser window. Elements do not move as window is scrolled.
  - floating elements: takes element out of normal flow and is placed to far the right or left.
- overlapping elements can be made with z index, the lower the index, the lower the z position
- floats often need to be cleared, says that element within the same containing element, should touch the right or left side of a box. clear: left, right, or both
- if all the elements in a parent container float, the browser may reduce the container to zero
  - set overflow to auto, and width to 100%
- liquid layout stretches and contracts as browser changes.
- fixed layout, width specified in pixels, stays the same width
