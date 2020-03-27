

# Responsive Web Design and SMACSS #

**Responsive Web Design**
- The wide variety of screen sizes, from phones to tablets to desktops, requires that able a website be able to handle different size screens.
- the answer to this is Repsonsize Web Design (RWD)
- Responsive vs Adaptive vs mobile
  - Responsive: responds postively and quickly to change.
  - Adaptable: easy to modify for new situation
  - Mobile: having a separate page for mobile devices
  - combination of the first two is best
- RWD is broken down in three parts, flexible layout, media queries, and flexible media
- Flexible Layout
  - building layout on flexible grid, able to resize dynamically to any size
  - uses relative lengths, such as percentages or em, not pixels or inches
  - percentage forumla: target width / parent width = result
- Media Queries
- provide the ability to specify different styles for diffrent circumstanes/screens
- media rule: @media all and (max-width: 1024px) {...}
- use logical operators to combine conditions, @media all and (min-width: 500px) and (max-width 1024) {...}
- can be used to check if screen is in landscape or portrait orientation: @media (orientation: landscape) {...}
- can also check for aspect ration, or resolution 
- main example: switching layout from double column to one when max width is 420px
- Mobile first: a technique used with media enquires to insure that mobile devices do not need to load more than they need to
 - organize media queries with mobile versions first
 - when making moblie styles, consider simplyfing layout, removing background image etc
- Flexible Media
  - when viewport scales, media do not always follow suit
  - one easy way is to use max-width: 100%;
  - won't always work with iframes and embedded media
  - there is a workaround
    - embedded media must be absolutely positioned within parent element
    - parent element: width:100%, height: 0; padding-bottom %

**All about Floats**
- made after concept in print layout, how the text will wrap around pictures and other features
- floated elements remains in the page's flow
- float values: left, right, none, inherit (will assume the float value from the elements parents element)
- used for text-wrapping, and creatinging layouts.
- can also be useful for arranging elements within smaller containers
- Clear: sister property to float
- an element with clear property will not jump up to be adjecent with the floated element, like when the footer jumps up
- Clear values: left, right, both, none(when would you use this one?)
- if all the children of an element are floated, that element will collapse, 0 height
- how to fix 
  - clear: both
  - empty div method: `<div style="clear: both;"></div>`
  - overflow method: setting overflow property to auto or hidden to parent element
  - the 'easy' clearing method: apply class .clearfix to parent then 

    ```
     .clearfix:after { 
        content: "."; 
        visibility: hidden; 
        display: block; 
        height: 0; 
        clear: both;
    }

   ```
